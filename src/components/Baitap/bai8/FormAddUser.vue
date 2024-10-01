<template>
    <div v-if="isVisible" class="form-container">
      <h3>Form Add User</h3>
      <form @submit.prevent="submitForm">
        <div>
          <label>Name:</label>
          <input type="text" v-model="name" required />
        </div>
        <div>
          <label>Email:</label>
          <input type="email" v-model="email" required />
        </div>
        <div>
          <label>Address:</label>
          <input type="text" v-model="address" required />
        </div>
        <button type="button" @click="closeForm">Close</button>
        <button type="submit">Submit</button>
      </form>
    </div>
  </template>
  
  <script setup>
  import { ref, defineEmits } from 'vue';
  
  const isVisible = ref(false);
  const name = ref('');
  const email = ref('');
  const address = ref('');
  
  const emit = defineEmits();
  
  const closeForm = () => {
    isVisible.value = false;
  };
  
  const submitForm = () => {
    // Handle form submission logic here
    console.log({ name: name.value, email: email.value, address: address.value });
    closeForm();
  };
  
  const openForm = () => {
    isVisible.value = true;
  };
  
  export { isVisible, openForm };
  </script>
  
  <style scoped>
  .form-container {
    border: 1px solid #ccc;
    padding: 20px;
    margin-top: 20px;
  }
  </style>