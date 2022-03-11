<template>
  <NuxtLink to="/" class="logo">
    <img class="logo__image" height="32px" :src="logoPath" alt="Logo de ABACO">
  </NuxtLink>
</template>
<script setup>
const props = defineProps({
  color: {
    type: String,
    required: false,
    default: "normal",
    validator: (value) => ["light", "normal","white"].includes(value)
  }
})

const logoPath =
  `/abaco_logo${ props.color === "normal" ? "" : "_" + props.color }.png`
</script>
<style>
.logo {
  line-height: 0;
}
</style>
