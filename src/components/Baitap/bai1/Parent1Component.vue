<template>
    <div>
      <h1>Parent Component</h1>
      <Children1Component :companyName="companyName" />
    </div>
  </template>
  
  <script setup>
        const companyName = 'Rikkei Academy';
        import Children1Component from './Children1Component.vue';
  </script>
  
  <style scoped>
  h1 {
    color: blue;
  }
  </style>