<template>
    <div>
      <button @click="sendMessage">Send message</button>
    </div>
  </template>
  
  <script setup>
  import { defineEmits } from 'vue';
  
  const emit = defineEmits();
  
  const sendMessage = () => {
    emit('messageSent', 'Welcome to Rikkei Education');
  };
  </script>
  
  <style scoped>
  button {
    padding: 10px 20px;
    font-size: 16px;
  }
  </style>