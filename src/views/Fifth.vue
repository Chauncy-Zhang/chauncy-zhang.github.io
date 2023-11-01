<script setup>
import { ref } from 'vue';

const awesome = ref(true)
const div5 = ref("div5")

function toggle() {
    awesome.value = !awesome.value
}

</script>
<template>
    <div :class="div5">
        <button @click="toggle">toggle</button>
        <h1 v-if="awesome">Vue is awesome!</h1>
        <h1 v-else>Oh no 😢</h1>
    </div>
</template>
<style>
.div5 {
    /* margin-right: auto; */
    /* width: 500px; */
    color: aqua;border-style: solid;
    width: auto;
}
</style>