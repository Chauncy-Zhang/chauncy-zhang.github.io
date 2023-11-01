<script setup>
import { reactive, ref } from 'vue';

const counter = reactive({ count: 0 })
counter.count++
const message = ref('hello world!!!')
message.value = 'Changed'
const div1 = ref('div1')
</script>
<template>
    <div :class="div1">
        <h1>{{ message.split('').reverse().join('') }}</h1>
        <p>count is : {{ counter }}</p>
    </div>
</template>
<style>
.div1 {
    border-style: solid;
    width: auto;

}
</style>