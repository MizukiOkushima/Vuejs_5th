<script setup>
// import { watch, watchEffect } from 'vue';

// const props = defineProps(['foo', 'bar'])
// const { foo } = defineProps(['foo'])
// console.log(props.foo)
// props.foo = 'hi' // propsはリードオンリーのため子コンポーネント側から変更するこは不可
// watchEffect(() => {
//     console.log(foo)
// })
// watch(
//     () => foo,
//     () => {
//         console.log('watch')
//     })

defineProps({
    // foo: Number
    foo: {
        type: Number,   // 型
        // type: [Number, String, Boolean, Array, Object, Function, Symbol, Date, CustomClass],
        // type: Boolean,
        required: true, // 親propsにて必ず指定する必要があるようにする
        // default: 100,   // デフォルト値 requiredがtrueの場合、同時に宣言することはない
        // default: function() {
        //     return 100
        // }
        // validator: function (value) { // false 警告をコンソールに表示 true 警告をコンソールに表示しない
        validator(value) { // false 警告をコンソールに表示 true 警告をコンソールに表示しない
            // return false
            return value === 0 || value === 1
        }
    },
    bar: {
        type: String,
    },
    totalScore: {
        type: Number,
        required: true,
        validator(value) {
            return value === 0 || value === 1
        }
    },
})

</script>
<template>
    <!-- <p>count: {{ foo }}</p> -->
    <!-- <p>{{ bar }}</p>
    <p>{{ $attrs }}</p> -->
    <!-- <p>Count: {{ foo === undefined }}</p> -->
    <!-- <p>Count: {{ foo === false }}</p> -->
    <p>Count: {{ totalScore }}</p>
</template>