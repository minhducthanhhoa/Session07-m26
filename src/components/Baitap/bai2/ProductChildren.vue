<template>
    <div>
      <h2>Dữ liệu trong component con</h2>
      <p>ID: {{ product.id }}</p>
      <p>Name: {{ product.name }}</p>
      <p>Price: ${{ product.price }}</p>
      <p>Quantity: {{ product.quantity }}</p>
    </div>
  </template>
  
  <script setup>
  import { defineProps } from 'vue';
  
  const props = defineProps({
    product: {
      type: Object,
      required: true,
    },
  });
  </script>
  
  <style scoped>
  h2 {
    color: green;
  }
  </style>