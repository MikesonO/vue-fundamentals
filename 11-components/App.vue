<script>

// Importing the child component to be used in this parent component
import ChildComp from './ChildComp.vue'
  
export default {
  // Registering the imported child component so it can be used in the template
  components: {
    ChildComp
  }
}
</script>

<template>
  <!-- Using the child component -->
 <ChildComp />
</template>