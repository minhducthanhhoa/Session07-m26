<template>
    <button>{{ props.title }}</button>
</template>

<script setup>
    const props = defineProps({
        title:{
            default: "Click me",
            type: String,
            required: true,
        }
    })
</script>

<style>

</style>