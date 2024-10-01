<template>
    <div>
      <MessageChildren @messageSent="handleMessage" />
      <div v-if="message" class="message-display">{{ message }}</div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import MessageChildren from './MessageChildren.vue';
  
  const message = ref('');
  
  const handleMessage = (msg) => {
    message.value = msg;
  };
  </script>
  
  <style scoped>
  .message-display {
    margin-top: 20px;
    font-size: 18px;
    color: blue;
  }
  </style>