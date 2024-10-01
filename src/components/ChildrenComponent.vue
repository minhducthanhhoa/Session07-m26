<template>
  <div>
    <h1>ChildrenComponent</h1>
    <h3>UserName of children: {{ props.userNameProps }}</h3>
    <h3>Age: {{ props.ageProps }}</h3>
  </div>

</template>

<script setup>
    const props = defineProps(["userNameProps", "ageProps", "userInfoProps"]);
</script>

<style>

</style>