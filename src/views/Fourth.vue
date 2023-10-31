<script setup>
    import {ref} from 'vue'
    const text = ref("")

    const ptext = ref("ptext")

    function onInput(e){
        text.value = e.target.value
    }

</script>
<template>
    <!-- <input :value="text" v-on:input="onInput"> -->
    <input v-model="text"/>
    <p :class ="ptext" >{{ text }}</p>
</template>
<style>
    .ptext {
        color: blue;
    }
</style>