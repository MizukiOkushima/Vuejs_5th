<script setup>
import { ref } from 'vue';
// const x = ref('x')
const pageCount = ref(1)
</script>
<template>
    <div>
        <!-- <h2>Hello</h2> -->
        <!-- <slot /> -->
        <!-- <slot>
            <p>No Content</p>
         </slot> -->
        <button @click="pageCount = 1">1</button>
        <button @click="pageCount = 2">2</button>
        <button @click="pageCount = 3">3</button>
        <header>
            <!-- <slot name="header" :page-count="pageCount" foo="foo" /> -->
            <slot name="header" :page-count="pageCount" />
        </header>
        <main>
            <!-- <slot name="main"/> -->
            <!-- <slot /> -->
            <slot :page-count="pageCount" />
        </main>
        <!-- <footer>
            <slot name="footer"/>
        </footer> -->
        <footer>
            <p>Instructor: Anonymous</p>
        </footer>
    </div>
</template>
<style scoped>
div {
    box-shadow: 2px 2px 6px rgba(0, 0, 0, 0.4);
    border-radius: 5px;
    padding: 16px;
}
</style>