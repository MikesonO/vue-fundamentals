<script setup>
import { ref } from 'vue'
import ChildComp from './ChildComp.vue'

const msg = ref('from parent')
</script>

<template>
  <!-- Passing content to the child component via the default slot -->
  <ChildComp>This message is {{ msg }}</ChildComp>
</template>