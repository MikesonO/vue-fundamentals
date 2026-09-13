<script>
import ChildComp from './ChildComp.vue'

export default {
  components: {
    ChildComp
  },
  data() {
    return {
      // Greeting message to be passed as a prop to the child component
      greeting: 'Hello from parent'
    }
  }
}
</script>

<template>
  <!-- Passing the greeting data as a prop to the child component -->
  <ChildComp :msg="greeting" />
</template>