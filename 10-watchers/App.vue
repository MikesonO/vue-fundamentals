<script setup>
import { ref, watch, onMounted } from 'vue'

// Component's reactive data properties
const todoId = ref(1)
const todoData = ref(null)

// Function for fetching data from the API based on the current todoId
async function fetchData() {
  todoData.value = null
  const res = await fetch(
    `https://jsonplaceholder.typicode.com/todos/${todoId.value}`
  )
  todoData.value = await res.json()
}

// Lifecycle hook called when the component is mounted (element exists in the DOM)
onMounted(() => {
  fetchData()
})

// Watcher for changes in the todoId reactive property
watch(todoId, () => {
  fetchData()
})

</script>

<template>
  <p>Todo id: {{ todoId }}</p>
  <button @click="todoId++" :disabled="!todoData">Fetch next todo</button>
  <p v-if="!todoData">Loading...</p>
  <pre v-else>{{ todoData }}</pre>
</template>