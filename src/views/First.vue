<script setup>
    import { reactive,ref } from 'vue';

    const counter = reactive({count:0})
    counter.count++
    const message = ref('hello world!!!')
    message.value = 'Changed'
</script>
<template>
    <h1>{{ message.split('').reverse().join('') }}</h1>
    <p>count is : {{ counter }}</p>
</template>