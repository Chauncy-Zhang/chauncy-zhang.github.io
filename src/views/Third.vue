<script setup>
import { ref } from 'vue'
const count = ref(0)
function increment() {
    count.value++
}
const div3 = ref("div3")
</script>
<template>
    <div :class="div3">
        <button @click="increment">count is :{{ count }}</button>
    </div>
</template>
<style>
.div3 {
    border-style: solid;
    width: auto;

}
</style>