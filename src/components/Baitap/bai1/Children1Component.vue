<template>
    <div>
      <h2>Children Component</h2>
      <p>Company Name: {{ companyName }}</p>
    </div>
  </template>
  
  <script setup>
  import { defineProps } from 'vue';
  
  const props = defineProps({
    companyName: {
      type: String,
      required: true,
    },
  });
  </script>
  
  <style scoped>
  h2 {
    color: green;
  }
  </style>