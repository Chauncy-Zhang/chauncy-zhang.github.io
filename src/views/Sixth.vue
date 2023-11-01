<script setup>
import { ref, computed } from 'vue';
let id = 0
const newTodo = ref()
const hideCompleted = ref(false)
const todos = ref(
    [
        { id: id++, text: 'learn html', done: false },
        { id: id++, text: 'learn javascript', done: false },
        { id: id++, text: 'learn vue', done: false }
    ]
)
function addTodo() {
    todos.value.push({ id: id++, text: newTodo.value })
}
function removeTodo(todo) {
    todos.value = todos.value.filter((x) => x !== todo)
}

const filteredTodos = computed(() => {
    // 根据 `todos.value` & `hideCompleted.value`
    // 返回过滤后的 todo 项目
    return hideCompleted.value ? todos.value.filter((t) => !t.done) : todos.value
})
const div6 = ref("div6")
</script>
<template>
    <div :class="div6">
        <form @submit.prevent='addTodo'>
            <input v-model="newTodo">
            <button>Add Todo</button>
        </form>
        <ul>
            <li v-for="todo in filteredTodos" v-bind:key="todo.id">
                <input type="checkbox" v-model="todo.done">
                <span v-bind:class="{ done: todo.done }">{{ todo.text }}</span>
                <button @click="removeTodo(todo)">X</button>
            </li>
        </ul>
        <button @click="hideCompleted = !hideCompleted">
            {{ hideCompleted ? 'Show all' : 'Hide completed' }}
        </button>
    </div>
</template>
<style>
.div6 {
    border-style: solid;
    width: auto;

}

.done {
    text-decoration: line-through;
}</style>