<script setup>
import first from "./views/First.vue"
import second from "./views/second.vue"
import third from "./views/Third.vue"
import fourth from "./views/Fourth.vue"
import fifth from "./views/Fifth.vue"
import sixth from "./views/Sixth.vue"
import seventh from "./views/Seventh.vue"
import eighth from "./views/Eighth.vue"
import ninth from "./views/Ninth.vue"
import tenth from "./views/Tenth.vue"
import Eleventh from "./views/Eleventh.vue"
import { ref } from "vue"

const greeting = ref("hello from parent")
const childMsg = ref('No child msg yet')
const  msg = ref('from  parent')

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
      <ninth :msg="greeting" />
      <Eleventh>msg：{{ msg }}</Eleventh>
    </div>
    <div :class="div02">
      <second />
      <fourth />
      <sixth />
      <eighth />
      <tenth @response="(msg) => childMsg = msg" />
      <p>{{ childMsg }}</p>
    </div>
  </div>
</template>
<style>
.div0 {
  width: 200%;
  height: auto;
  border-style: solid;
}

.div01 {
  width: auto;
  border-style: solid;
  float: left;
}

.div02 {
  width: auto;
  border-style: solid;
  float: right;
}


.htext {
  text-align: center;
}
</style>