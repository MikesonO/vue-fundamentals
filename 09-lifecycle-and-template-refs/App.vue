<script>
export default {
  
  // Lifecycle hook called when the component is mounted (element exists in the DOM)
  mounted() {
    this.$refs.pElementRef.textContent = "Mounted test"
  }
}
</script>

<template> 
  <p ref="pElementRef">Hello</p>
</template>
