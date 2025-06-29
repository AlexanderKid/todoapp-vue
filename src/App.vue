<template>
  <div class="min-h-screen bg-gray-100 p-6 flex flex-col items-center">
    <h1 class="text-3xl font-bold text-indigo-600 mb-6">📝 ToDo App</h1>

    <form @submit.prevent="addTodo" class="flex gap-2 mb-6 w-full max-w-md">
      <input
        v-model="newTask"
        placeholder="Enter a task..."
        class="p-2 w-full border border-gray-300 rounded shadow-sm focus:outline-none focus:ring-2 focus:ring-indigo-500"
      />
      <button
        type="submit"
        class="bg-indigo-600 text-white px-4 py-2 rounded hover:bg-indigo-700"
      >
        Add
      </button>
    </form>

    <ul class="w-full max-w-md space-y-2">
      <li
        v-for="(todo, index) in todos"
        :key="index"
        class="bg-white p-4 rounded shadow flex justify-between items-center"
      >
        <span :class="{ 'line-through text-gray-400': todo.done }" @click="toggleTodo(index)" class="cursor-pointer">
          {{ todo.text }}
        </span>
        <button @click="deleteTodo(index)" class="text-red-500 hover:underline">Delete</button>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref, watch } from 'vue'

const newTask = ref('')
const todos = ref([])

// завантажуємо з localStorage
if (localStorage.getItem('todos')) {
  todos.value = JSON.parse(localStorage.getItem('todos'))
}

// записуємо в localStorage при зміні
watch(todos, (newVal) => {
  localStorage.setItem('todos', JSON.stringify(newVal))
}, { deep: true })

function addTodo() {
  if (newTask.value.trim()) {
    todos.value.push({ text: newTask.value, done: false })
    newTask.value = ''
  }
}

function deleteTodo(index) {
  todos.value.splice(index, 1)
}

function toggleTodo(index) {
  todos.value[index].done = !todos.value[index].done
}
</script>

<style>
body {
  margin: 0;
  font-family: system-ui, sans-serif;
}
</style>