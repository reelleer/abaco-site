<template>
  <header class="header">
    <div class="container">
      <AppLogo color="light" />
      <TheMenu class="header__menu" :class="menuClass" />
      <svg class="header__mobile-icon" @click="toggleMenu" xmlns="http://www.w3.org/2000/svg" width="32" height="32" fill="currentColor" viewBox="0 0 16 16">
          <path fill-rule="evenodd" d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"/>
      </svg>
    </div>
  </header>
</template>
<script setup>
import { ref, computed } from "vue"

const isOpen = ref(false)

const menuClass = computed(() => isOpen.value ? "header__menu--display" : "")

const toggleMenu = () => isOpen.value = !isOpen.value
</script>
<style>
.header {
  background-color: var(--background-color);
  height: 3.375rem;
}

.header .container {
  --calc-padding-top-bottom: calc((54px - 32px) / 2);
  display: flex;
  justify-content: space-between;
  padding-bottom: var(--calc-padding-top-bottom);
  padding-top: var(--calc-padding-top-bottom);
}

.header__menu {
  display: none;
}

.header__menu--display {
  display: block;
  left: 0px;
  position: absolute;
  top: 54px;
  width: 100%;
}

.header__mobile-icon {
  color: white;
}
</style>
