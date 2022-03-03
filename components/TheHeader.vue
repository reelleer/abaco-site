<template>
  <header class="header">
    <div class="container">
      <AppLogo color="light" />
      <TheMenu class="header__menu" :class="menuClass" />
      <AppIcon
        class="header__mobile-icon"
        :name="iconName"
        @click="toggleMenu"
      />
    </div>
  </header>
</template>
<script setup>
import { ref, computed } from "vue"

const isOpen = ref(false)

const menuClass = computed(() => isOpen.value ? "header__menu--display" : "")
const iconName = computed(() => isOpen.value ? "x-lg" : "list")

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
  z-index: 100;
}

.header__mobile-icon {
  color: white;
  width: 32px;
  height: 32px;
}

@media only screen and (min-width: 768px) {
  .header {
    height: 5.125rem;
  }

  .header__menu {
    display: block;
  }

  .header__mobile-icon {
    display: none;
  }
}
</style>
