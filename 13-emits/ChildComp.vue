<script>
export default {
  // Declaring the events that this component can emit to its parent
  emits: ['response'],
  created() {
    // Emitting the 'response' event with a message when the component is created
    this.$emit('response', 'hello from child')
  }
}
</script>

<template>
  <h2>Child component</h2>
</template>