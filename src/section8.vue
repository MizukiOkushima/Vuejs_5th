<script setup>
import { ref } from 'vue';
import CountUp from './components/CountUpSection8.vue'
const isShow = ref(true)
</script>
<template>
    <button @click="isShow = !isShow">switch</button>
    <CountUp v-if="isShow" />
</template>