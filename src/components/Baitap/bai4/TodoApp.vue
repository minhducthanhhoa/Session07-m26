<template>
    <div>
      <h1>Todo App</h1>
      <ul>
        <li v-for="item in todos" :key="item.id">
          {{ item.name }}
          <TodoItem :id="item.id" @delete="handleDelete" />
        </li>
      </ul>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import TodoItem from './TodoItem.vue';
  
  const todos = ref([
    { id: 1, name: 'Learn Vue 3' },
    { id: 2, name: 'Build a project' },
    { id: 3, name: 'Read documentation' },
  ]);
  
  const handleDelete = (id) => {
    todos.value = todos.value.filter(item => item.id !== id);
  };
  </script>
  
  <style scoped>
  h1 {
    color: blue;
  }
  </style>