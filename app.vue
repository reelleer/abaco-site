<template>
  <TheHeader />
    <NuxtLayout>
      <main>
        <NuxtPage />
      </main>
    </NuxtLayout>
  <TheFooter />
</template>
<script setup>
useMeta({
  link: [
    {rel: 'icon', type: 'image/png', sizes: '16x16', href: '/favicon-16x16.png'},
    {rel: 'icon', type: 'image/png', sizes: '32x32', href: '/favicon-32x32.png'}
  ],
  title: "ABACO",
  htmlAttrs: {
    lang: "es-ni"
  }
})
</script>
<style>
@import "./assets/styles/main.css"
</style>
