<script setup>
    import { ref } from 'vue';

    const titleClass = ref('title')
    const div2 = ref('div2')
</script>
<template>
    <div :class="div2">
        <h1 :class="titleClass">make me red</h1>
    </div>
</template>
<style>
    .div2{border-style: solid;    width: auto;

    }
    .title{
        color: red;
    }
</style>