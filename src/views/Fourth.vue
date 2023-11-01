<script setup>
import { ref } from 'vue'
const text = ref("")

const ptext = ref("ptext")

function onInput(e) {
    text.value = e.target.value
}
const div4 = ref("div4")

</script>
<template>
    <div :class="div4">
        <!-- <input :value="text" v-on:input="onInput"> -->
        <input v-model="text" />
        <p :class="ptext">{{ text }}</p>
    </div>
</template>
<style>
.div4 {
    border-style: solid;
    width: auto;

}

.ptext {
    color: blue;
}
</style>