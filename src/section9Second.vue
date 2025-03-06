<script setup>
import { ref, shallowRef } from 'vue'
import CompA from './components/CompA.vue'
import CompB from './components/CompB.vue'
import CompC from './components/CompC.vue'
// const currentComp = ref(CompA)
const currentComp = shallowRef(CompA)
console.log(currentComp.value)
// const tmpObj = shallowRef({
//     count: 0,
// })
// const tmpObj = shallowRef({})
</script>
<template>
    <h1>Dynamic Components</h1>
    <button @click="currentComp = CompA">A</button>
    <button @click="currentComp = CompB">B</button>
    <button @click="currentComp = CompC">C</button>
    <!-- <component :is="CompA" /> -->
    <!-- <KeepAlive :include="CompB"> -->
    <!-- <KeepAlive :include="CompA,CompC"> -->
    <!-- <KeepAlive :include="['CompA','CompC']"> -->
    <!-- <KeepAlive :exclude="['CompA','CompC']"> -->
    <!-- <KeepAlive :max="2"> -->
    <KeepAlive>
        <component :is="currentComp" />
    </KeepAlive>
    <!-- <KeepAlive>
        <CompB v-if="currentComp === CompB" />
        <CompB v-else />
    </KeepAlive> -->
    <!-- <CompB v-show="currentComp === CompB" /> -->
    <!-- <p>{{ tmpObj }}</p>
    <button @click="tmpObj = {}">+1</button> -->
    <Teleport to="body">
        <h2>Teleport</h2>
    </Teleport>
</template>
