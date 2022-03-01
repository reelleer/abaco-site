<template>
  <svg class="icon" width="16" height="16" fill="currentColor">
    <use :href="nameRef" />
  </svg>
</template>
<script setup>
import { ref, watchEffect } from "vue"

const props = defineProps({
  name: {
    type: String,
    required: true,
    validator: (value) => 
      ["envelope", "geo-alt", "telephone", "list", "x-lg"].includes(value)
  }
})

const nameRef = ref("")

watchEffect(() => nameRef.value = `#${props.name}`) 
</script>
