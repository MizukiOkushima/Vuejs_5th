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
const isShow = ref(false)
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
    <!-- <Teleport to="#app"> -->
    <!-- <Teleport to=".app"> -->
    <button @click="isShow = true">Open Modal</button>
    <Teleport to="body" :disabled="true">
        <!-- <Teleport to="body" :disabled="false"> -->
        <!-- <Teleport to="body"> -->
        <!-- <h2>Teleport</h2>
        <p>{{ currentComp === CompA }}</p> -->
        <dialog v-if="isShow" open>
            <p>This is a Modal!</p>
            <button @click="isShow = false">Close</button>
        </dialog>
    </Teleport>
    <!-- <Teleport to="body" defer><p>A</p></Teleport> -->
    <!-- <Teleport to="#compB" defer><p>A</p></Teleport> -->
    <Teleport to="#compA" defer><p>A</p></Teleport>
    <Teleport to="body"><p>B</p></Teleport>
</template>