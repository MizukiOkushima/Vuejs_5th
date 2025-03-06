<script setup>
// import { ref } from 'vue';
import BaseCard from './components/BaseCard.vue';
// const y = ref('y')
</script>
<template>
    <h1>Slots</h1>
    <!-- <BaseCard>
        <h2>Hello</h2>
        <p>How are you?</p>
        <p>{{ x }}</p>
        <p>{{ y }}</p>
    </BaseCard> -->
    <!-- <BaseCard>
        <ul>
            <li>Apple</li>
            <li>Banana</li>
            <li>Grape</li>
        </ul>
    </BaseCard> -->
    <!-- <BaseCard /> -->
    <!-- <BaseCard>
        <h2>Hello</h2>
        <p>How are you?</p>
    </BaseCard> -->
    <!-- <BaseCard> -->
    <!-- <template v-slot:header></template>
<template v-slot:main></template>
<template vsolt:footer></template> -->
    <!-- <template #header="slotProps">
            <p>{{ slotProps }}</p>
            <p>pageCount: {{ slotProps.pageCount }}</p>
            <p>foo: {{ slotProps.foo }}</p>
            <h2>Vue.js Corse</h2>
        </template> -->
    <!-- <template #header="{ pageCount }">
            <h2 v-if="pageCount == 1">Vue.js Corse</h2>
            <h2 v-if="pageCount == 2">HTML Corse</h2>
            <h2 v-if="pageCount == 3">CSS Corse</h2>
        </template> -->
    <!-- <template #default>
            <p>This is a Vue.js Course. You can learn Vue.js.</p>
        </template> -->
    <!-- <p>This is a Vue.js Course. You can learn Vue.js.</p>
        <p>Hello</p> -->
    <!-- <template #default="{ pageCount }">
            <p v-if="pageCount === 1">This is a Vue.js Course. You can learn Vue.js.</p>
            <p v-if="pageCount === 2">This is a HTML Course. You can learn Vue.js.</p>
            <p v-if="pageCount === 3">This is a CSS Course. You can learn Vue.js.</p>
        </template>
        <template #footer> -->
    <!-- <p>Instructor: HogeOjisan</p> -->
    <!-- </template>
    </BaseCard> -->

    <BaseCard v-slot="{ pageCount }">
        <h2 v-if="pageCount == 1">Vue.js Corse</h2>
        <h2 v-if="pageCount == 2">HTML Corse</h2>
        <h2 v-if="pageCount == 3">CSS Corse</h2>
        <p v-if="pageCount === 1">This is a Vue.js Course. You can learn Vue.js.</p>
        <p v-if="pageCount === 2">This is a HTML Course. You can learn Vue.js.</p>
        <p v-if="pageCount === 3">This is a CSS Course. You can learn Vue.js.</p>
        <p>Instructor: HogeOjisan</p>
    </BaseCard>

</template>