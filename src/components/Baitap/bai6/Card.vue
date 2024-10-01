<template>
    <div class="card">
      <div class="card-header">
        <slot name="header"></slot>
      </div>
      <div class="card-body">
        <slot name="body"></slot>
      </div>
      <div class="card-footer">
        <slot name="footer"></slot>
      </div>
    </div>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  .card {
    border: 1px solid #ddd;
    border-radius: 5px;
    padding: 20px;
    margin: 10px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  }
  
  .card-header {
    font-weight: bold;
    font-size: 1.2em;
  }
  
  .card-body {
    margin: 10px 0;
  }
  
  .card-footer {
    text-align: right;
  }
  </style>