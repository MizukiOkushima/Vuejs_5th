<script setup>
import {
    ref,
    onBeforeMount,
    onMounted,
    onBeforeUpdate,
    onUpdated,
    onBeforeUnmount,
    onUnmounted,
    nextTick,
} from 'vue';
const count = ref(0)
console.log('script setup')
onBeforeMount(() => {
    console.log('onBeforeMount')
    // debugger
})
onMounted(() => {
    console.log('onMounted')
    // debugger
})
onBeforeUpdate(() => {
    console.log('onBeforeUpdate')
    // debugger
})
onUpdated(() => {
    console.log('onUpdated')
    // debugger
})
onBeforeUnmount(() => {
    console.log('onBeforeUnmount')
    // debugger
})
onUnmounted(() => {
    console.log('onUnmounted')
    // debugger
})
// function countUp() {
//     count.value++
//     count.value++
//     count.value++
//     nextTick(() => {
//         console.log('nextTick')
//         debugger
//     })
//     // debugger
// }
async function countUp() {
    count.value++
    count.value++
    count.value++
    await nextTick()
    console.log('nextTick')
    debugger
}
</script>
<template>
    <p>count: {{ count }}</p>
    <!-- <button @click="count++">+1</button> -->
    <button @click="countUp">+1</button>
</template>