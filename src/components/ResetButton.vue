<script setup>
// defineEmits(['reset'])
// const emit = defineEmits(['reset'])
// function emitReset() {
//     emit('reset', 100)
// }
const emit = defineEmits(['resetCount'])
function emitReset() {
    emit('resetCount', 100)
}
</script>
<template>
    <button @click="emitReset">Reset</button>
</template>