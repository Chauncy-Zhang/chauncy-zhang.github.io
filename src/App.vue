<script setup>
import first from "./views/First.vue"
import second from "./views/second.vue"
import third from "./views/Third.vue"
import fourth from "./views/Fourth.vue"
import fifth from "./views/Fifth.vue"
import sixth from "./views/Sixth.vue"
import seventh from "./views/Seventh.vue"
import { ref } from "vue"

const div0 = ref("div0")
const div01 = ref("div01")
const div02 = ref("div02")
const htext = ref("htext")
</script>

<template>
  <div :class="div0">
    <h1 :class="htext">Hello world</h1>
    <div :class="div01">
      <first />
      <third />
      <fifth />
      <seventh />
    </div>
    <div :class="div02">
      <second />
      <fourth />
      <sixth />
    </div>
  </div>
</template>
<style>
.div0 {
  width: auto;
  height: auto;
  border-style: solid;
  display: flex;
  justify-content: space-between;
}

.div01 {
  width: auto;
  border-style: solid;
}

.div02 {
  width: auto;
  border-style: solid;
}


.htext {
  text-align: center;
}
</style>