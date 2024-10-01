<template>
    <div id="app">
      <button @click="showModal">Show Modal</button>
      <Modal v-if="isModalVisible" @close="isModalVisible = false">
        <template #header>
          Thông báo từ hệ thống
        </template>
        <template #body>
          Đây là nội dung của modal. Bạn có thể đóng modal bằng cách nhấn vào nút 'Close'.
        </template>
      </Modal>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import Modal from './Modal.vue';
  
  const isModalVisible = ref(false);
  
  const showModal = () => {
    isModalVisible.value = true;
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