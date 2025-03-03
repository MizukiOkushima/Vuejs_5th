<script setup>
import CountUp from '@/components/CountUp.vue'
import BaseButton from './components/BaseButton.vue'
</script>
<template>
    <h1 class="red">App</h1>
    <p>Hello</p>
    <BaseIcon v-if="true" />
    <!-- <BaseIcon v-show="false" /> -->
    <!-- <BaseIcon id="base-button" class="border" /> -->
    <CountUp v-if="true" id="base-button" class="border" />
    <!-- <CountUp></CountUp>
    <count-up /> -->
    <BaseButton v-if="true" id="base-button" class="border" @click="console.log('BaseButton.vue')" />
    <BaseButton v-show="false" id="base-button" class="border" @click="console.log('BaseButton.vue')" />
</template>
<style>
/* body {
    background-color: beige;
} */
</style>
<style scoped>
.red {
    color: red;
}
</style>