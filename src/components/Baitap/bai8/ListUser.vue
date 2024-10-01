<template>
    <div>
      <h2>------- List User -------</h2>
      <button @click="openForm">Add user</button>
      <FormAddUser ref="formAddUser" />
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import FormAddUser from './FormAddUser.vue';
  
  const formAddUser = ref(null);
  
  const openForm = () => {
    formAddUser.value.openForm();
  };
  </script>
  
  <style scoped>
  button {
    padding: 10px 20px;
    font-size: 16px;
  }
  </style>