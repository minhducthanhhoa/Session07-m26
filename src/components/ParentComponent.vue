<template>
  <div>
    <h1>Parent component</h1>
    <h3>UserName: {{ userName }}</h3>
    <p>____________________</p>
    <ChildrenComponent :userNameProps="userName" :ageProps="age" :userInfoProps="userInfo"></ChildrenComponent>
  </div>
</template>

<script setup>
    import ChildrenComponent from './ChildrenComponent.vue';
    const userName = "nguyễn văn a";
    const age = 20;
    const userInfo = {
        id: 1,
        name: "Nguyễn Văn B",
        age: 21,
    }
</script>

<style>

</style>