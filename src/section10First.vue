<script setup>
import { ref } from 'vue';
const userINput = ref('')
const message = ref('')
// const checked = ref(false)
const checked = ref('not checked')
// const fruits = ref(false)
const fruits = ref([])
const gender = ref('male')
// const selected = ref("A")
const selected = ref("")
</script>
<template>
    <h1>v-model</h1>
    <h2>Text</h2>
    <!-- <input v-model="userINput" type="text"> -->
    <!-- <input v-model.lazy="userINput" type="text"> -->
    <!-- <input v-model.lazy.trim="userINput" type="text"> -->
    <!-- <input v-model.lazy.trim.number="userINput" type="text"> -->
    <input v-model.lazy.trim="userINput" type="number">
    <p>{{ userINput }}</p>
    <p>{{ typeof userINput }}</p>
    <h2>Textarea</h2>
    <!-- <textarea v-model="message"></textarea> -->
    <textarea v-model.trim="message"></textarea>
    <p style="white-space: pre">{{ message }}</p>
    <input id="checkbox" v-model="checked" type="checkbox" true-value="checked" false-value="not checked">
    <label for="checkbox">{{ checked }}</label>
    <p>Fruits</p>
    <input id="Apple" v-model="fruits" type="checkbox" value="Apple" />
    <label for="Apple">Apple</label>
    <input id="Banana" v-model="fruits" type="checkbox" value="Banana" />
    <label for="Banana">Banana</label>
    <input id="Grape" v-model="fruits" type="checkbox" value="Grape" />
    <label for="Grape">Grape</label>
    <p>{{ fruits }}</p>
    <h2>Radio</h2>
    <input id="male" v-model="gender" type="radio" value="male">
    <label for="male">male</label>
    <input id="female" v-model="gender" type="radio" value="female">
    <label for="female">female</label>
    <p>{{ gender }}</p>
    <h2>Select</h2>
    <!-- <select v-model="selected"> -->
    <select v-model="selected" multiple>
        <option value="" disabled>Select one</option>
        <!-- <option>A</option>
        <option>B</option>
        <option>C</option> -->
        <option v-for="option in ['A', 'B', 'C']" :key="option">{{ option }}</option>
    </select>
    <p>{{ selected }}</p>
</template>