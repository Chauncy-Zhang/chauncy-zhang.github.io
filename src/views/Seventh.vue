<script setup>
import { ref, onMounted } from 'vue';
const pElementRef = ref(null)
onMounted(() => {
    // 此时组件已经挂载。
    pElementRef.value.textContent = 'mounted!'
})
const div7 = ref("div7")
</script>
<template>
    <div :class="div7">
        <p ref="pElementRef">hello</p>

    </div>
</template>
<style>
.div7 {
    border-style: solid;
    width: auto;

}
</style>