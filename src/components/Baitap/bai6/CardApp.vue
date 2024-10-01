<template>
    <div id="app">
      <Card>
        <template #header>
          Thông tin sản phẩm
        </template>
        <template #body>
          Đây là mô tả ngắn gọn về sản phẩm này. Sản phẩm có các tính năng nổi bật và giá cả hợp lý.
        </template>
        <template #footer>
          <button @click="viewDetails">Xem chi tiết</button>
        </template>
      </Card>
    </div>
  </template>
  
  <script setup>
  import Card from './Card.vue';
  const viewDetails = () => {
    alert('Hiển thị thông tin chi tiết sản phẩm.');
  };
  </script>
  
  <style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  </style>