<script setup>
// Defining the events that this component can emit to its parent
const emit = defineEmits(['response'])

// Emitting the 'response' event with a message to the parent component
emit('response', 'hello from child')
</script>

<template>
  <h2>Child component</h2>
</template>