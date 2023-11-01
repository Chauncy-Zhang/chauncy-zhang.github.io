<script setup>
import { ref } from 'vue';

const awesome = ref(true)
const div1 = ref("div1")

function toggle() {
    awesome.value = !awesome.value
}

</script>
<template>
    <div :class="div1">
        <button @click="toggle">toggle</button>
        <h1 v-if="awesome">Vue is awesome!</h1>
        <h1 v-else>Oh no 😢</h1>
    </div>
</template>
<style>
    .div1 {
        /* margin-right: auto; */
        /* width: 500px; */
        color: aqua;
    }
</style>