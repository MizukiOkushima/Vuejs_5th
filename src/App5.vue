<script setup>
import { ref } from 'vue';
import ShowCount from './components/ShowCount.vue';
import ResetButton from './components/ResetButton.vue';
const count = ref(0)
function onReset(value) {
    count.value = value
}
</script>
<template>
    <!-- <ShowCount :foo="count" bar="hello"/> -->
    <!-- <ShowCount v-bind="{ foo: count, bar: 'hello' }" /> -->
    <!-- <ShowCount v-bind="{ bar: 'hello' }" /> -->
    <!-- <ShowCount bar="hello" /> -->
    <!-- <ShowCount foo bar="hello" /> fooをboolean型としてtrueを宣言したのと同じ記述 -->
    <!-- <ShowCount :foo="false" bar="hello" /> -->
    <!-- <ShowCount :foo="count" bar="hello" /> -->
    <!-- <ShowCount :totalScore="count" bar="hello" /> -->
    <ShowCount :total-score="count" bar="hello" />
    <button @click="count++">+1</button>
    <!-- <ResetButton @reset="count = 0"/> -->
    <!-- <ResetButton @reset="count = $event" /> -->
    <!-- <ResetButton @resetCount="onReset" /> -->
    <ResetButton @reset-count="onReset" />
</template>