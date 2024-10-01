<template>
    <div>
      <h1>Product Parent Component</h1>
      <ProductChildren :product="product" />
    </div>
  </template>
  
  <script setup>
        import ProductChildren from './ProductChildren.vue';
        const product = {
            id: 1,
            name: 'Laptop',
            price: 1200,
            quantity: 5
        };
  </script>
  
  <style scoped>
  h1 {
    color: blue;
  }
  </style>