<script>
import ChildComp from './ChildComp.vue'

export default {
  components: {
    ChildComp
  },
  data() {
    return {
      msg: 'from parent'
    }
  }
}
</script>

<template>
  <!-- Passing content to the child component via the default slot -->
  <ChildComp>This message is {{ msg }}</ChildComp>
</template>