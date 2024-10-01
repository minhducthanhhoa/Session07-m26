<template>
    <div class="modal-overlay" v-if="isVisible">
      <div class="modal">
        <div class="modal-header">
          <h3><slot name="header"></slot></h3>
          <button @click="closeModal">X</button>
        </div>
        <div class="modal-body">
          <slot name="body"></slot>
        </div>
        <div class="modal-footer">
          <button @click="closeModal">Close</button>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const props = defineProps();
  const emit = defineEmits();
  
  const isVisible = ref(true);
  
  const closeModal = () => {
    isVisible.value = false;
    emit('close');
  };
  </script>
  
  <style scoped>
  .modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .modal {
    background: white;
    padding: 20px;
    border-radius: 5px;
    width: 400px;
  }
  
  .modal-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .modal-body {
    margin: 10px 0;
  }
  
  .modal-footer {
    text-align: right;
  }
  </style>