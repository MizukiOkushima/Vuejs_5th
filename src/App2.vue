<script setup>
import { ref } from 'vue'

// const ok = ref(true)
// const maybeOk = ref(true)
// const maybeOk = ref(false)

// const fruits = ref(['Apple', 'Banana', 'Grape'])
const fruits = ref([
    { id: 1, name: 'Apple' },
    { id: 2, name: 'Apple' },
    { id: 3, name: 'Banana' },
    { id: 4, name: 'Grape' },
])

</script>
<template>

    <!-- <button @click="ok = !ok">toggle</button> -->

    <!-- <p v-if="ok">OK!</p>
    <p v-else-if="maybeOk">maybe OK!</p>
    <p v-else>not OK...</p> -->

    <!-- <template v-if="ok">
        <p>OK!</p>
        <p>Hello</p>
        <p>Hi</p>
    </template> -->

    <!-- <p v-show="ok">OK!</p>
    <p v-show="!ok">not OK...</p> -->

    <button @click="fruits.shift()">button</button>
    <!-- <li v-for="fruit in fruits" :key=fruit>
        <input type="text" />{{ fruit }}
    </li> -->
    <!-- <li v-for="fruit in fruits" :key=fruit.id>
        <input type="text" />{{ fruit.name }}
    </li> -->

    <!-- <li v-for="(fruit, index) in fruits" :key=fruit.id>
        <input type="text" />{{ fruit.name }}({{ index }})
    </li> -->

    <!-- <li v-for="({ id, name }, index) in fruits" :key=id>
        <input type="text" />{{ name }}({{ index }})
    </li> -->
    <template v-for="({ id, name }, index) in fruits" :key=id>
        <template v-if="id === 2">
            <p>id: {{ id }}</p>
            <input type="text" />{{ name }}({{ index }})
        </template>
    </template>

</template>