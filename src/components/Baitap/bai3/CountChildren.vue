<template>
    <div>
      <h2>Count Child Component</h2>
      <button @click="handleIncrement">Increment</button>
    </div>
  </template>
  
  <script setup>
  import { defineEmits } from 'vue';
  
  const emit = defineEmits();
  
  const handleIncrement = () => {
    emit('increment');
  };
  </script>
  
  <style scoped>
  h2 {
    color: green;
  }
  </style>