<template>
  <svg width="16" height="16" fill="currentColor">
    <use v-bind="attrs" />
  </svg>
</template>
<script setup>
import { ref, computed } from "vue"

const props = defineProps({
  name: {
    type: String,
    required: true,
    validator: (value) => 
      ["envelope", "geo-alt", "telephone", "list"].includes(value)
  }
})

const name = ref(props.name)

const attrs = computed(() => { return { href: `#${name.value}` } }) 
</script>
