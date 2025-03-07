<script setup>
import { ref } from 'vue'
import CustomInput from './components/CustomInput.vue'
const userInput = ref('hello')
const titleInput = ref('title')
</script>
<template>
    <h1>v-model</h1>
    <!-- <CustomInput v-model="userInput" /> -->
    <!-- <CustomInput v-model="userInput" v-model:titleName="titleInput" /> -->
    <CustomInput v-model="userInput" v-model:title-name="titleInput" />
    <!-- <button @click="userInput = 'hello'">hello</button> -->
    <p>userInput: {{ userInput }}</p>
    <p>titleInput: {{ titleInput }}</p>
</template>