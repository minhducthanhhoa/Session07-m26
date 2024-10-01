<template>
    <div>
      <button @click="handleDelete">Delete</button>
    </div>
  </template>
  
  <script setup>
  import { defineProps, defineEmits } from 'vue';
  
  const props = defineProps({
    id: {
      type: Number,
      required: true,
    },
  });
  
  const emit = defineEmits();
  
  const handleDelete = () => {
    emit('delete', props.id);
  };
  </script>
  
  <style scoped>
  button {
    color: red;
  }
  </style>