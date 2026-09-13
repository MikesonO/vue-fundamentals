<script>
export default {
  // Defining the props that this component expects to receive from its parent
  props: {
    msg: String
  }
}
</script>

<template>
  <!-- Displaying the message passed from the parent component -->
  <h2>{{ msg || 'No props passed yet' }}</h2>
</template>