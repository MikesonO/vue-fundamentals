<script>
export default {
  // Component's reactive data properties
  data() {
    return {
      todoId: 1,
      todoData: null
    }
  },
  // Methods for fetching data and handling component logic
  methods: {
    async fetchData() {
      this.todoData = null
      const res = await fetch(
        `https://jsonplaceholder.typicode.com/todos/${this.todoId}`
      )
      this.todoData = await res.json()
    }
  },
  // Lifecycle hook called when the component is mounted (element exists in the DOM)
  mounted() {
    this.fetchData()
  },
  // Watcher for todoId changes
  watch: {
    todoId() {
      this.fetchData()
    }
  }
}
</script>

<template>
  <p>Todo id: {{ todoId }}</p>
  <button @click="todoId++" :disabled="!todoData">Fetch next todo</button>
  <p v-if="!todoData">Loading...</p>
  <pre v-else>{{ todoData }}</pre>
</template>