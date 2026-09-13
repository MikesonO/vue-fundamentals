<script>
import ChildComp from './ChildComp.vue'

export default {
  components: {
    ChildComp
  },
  data() {
    return {
      childMsg: 'No child msg yet'
    }
  }
}
</script>

<template>
  <!-- Listening for the response event from the child component -->
  <ChildComp @response="(msg) => childMsg = msg" />
  <p>{{ childMsg }}</p>
</template>