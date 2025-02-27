<script setup>
import { ref, reactive } from 'vue'

// const userName = 'Hogehoge'
// console.log(userName)

const title = ref('Vue.js Course!')
// let price = 9.99

let price = ref(9.99)
console.log(price.value)

let a = 1
let b = 2
let c = a + b // c = 3
a = 4
console.log(c)

function increment() {
    // price += 1
    // console.log('clock!')
    price.value += 1
    console.log(price.value)

    instructor.age += 1
    instructor.bio = 'hi'
    instructor.sns.twitter = 'hello'
    instructor.email = ref('info@example.com')
}

const info = ref({
    students: 1000,
    rating: 4,
})
console.log(info.value.students)

const instructor = reactive({
    name: 'Hogehoge',
    age: 25,
    sns: {
        twitter: '@HogeTwi',
        youtube: '@HogeYouTube',
    },
    email: ref('sample@gmail.com'),
})
console.log(instructor.age)

instructor.bio = 'hello'
console.log(info.value)
console.log(instructor)

console.log(instructor.email)

const items = reactive([ref(1), ref(2), 3])
items.reverse()
console.log(items[0])
// console.log(items[0].value)

const courseInfo = {
    sections: ref(10),
    language: ref('Japanese'),
}
console.log(courseInfo.sections.value)

const sections = courseInfo.sections

</script>

<template>
    <h1>Title: {{ title }}</h1>
    <!-- <h2>Price: ${{ price - 1 }}</h2> -->
    <h2>Price: ${{ price }}</h2>
    <button @click="increment">button</button>
    <h2>Students: {{ info.students }}</h2>
    <h2>Instructor age: {{ instructor.age }}</h2>
    <h2>Instructor age: {{ instructor.bio }}</h2>
    <h2>Instructor SNS Twitter: {{ instructor.sns.twitter }}</h2>
    <h2>Instructor email: {{ instructor.email }}</h2>
    <h2>Course Info Sections: {{ courseInfo.sections.value }}</h2>
    <h2>Course Info Sections: {{ sections + 1 }}</h2>
</template>

<style>
/* h1 {
    color: red;
} */
</style>