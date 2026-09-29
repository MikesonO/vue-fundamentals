<script setup>
import { ref } from 'vue'
import ChildComp from './ChildComp.vue'

// Greeting message to be passed as a prop to the child component
const greeting = ref('Hello from parent')
</script>

<template>
  <!-- Passing the greeting ref as a prop to the child component -->
  <ChildComp :msg="greeting" />
</template>