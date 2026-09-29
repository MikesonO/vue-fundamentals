<script setup>
import { ref, onMounted } from 'vue'

const pElementRef = ref(null)

// Lifecycle hook called when the component is mounted (element exists in the DOM)
onMounted(() => {
  pElementRef.value.textContent = 'mounted!'
})
</script>

<template>
  <p ref="pElementRef">Hello</p>
</template>