<template>
    <div>
      <h1>Count Parent Component</h1>
      <p>Current Count: {{ count }}</p>
      <CountChildren @increment="incrementCount" />
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import CountChildren from './CountChildren.vue';
  
  const count = ref(0);
  
  const incrementCount = () => {
    count.value++;
  };
  </script>
  
  <style scoped>
  h1 {
    color: blue;
  }
  </style>