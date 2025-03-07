<script setup>
const model = defineModel({
    type: String,
    // required: true,
    default: 'default',
})
const titleName = defineModel('titleName', {
    type: String,
    required: true,
})
// model.value
</script>
<template>
    <h2>CustomInput</h2>
    <input v-model="model" type="text">
    <!-- <button @click="model = 'hi'">hi</button> -->
    <p>model: {{ model }}</p>
    <input v-model="titleName" type="text">
    <p>titleName: {{ titleName }}</p>
</template>