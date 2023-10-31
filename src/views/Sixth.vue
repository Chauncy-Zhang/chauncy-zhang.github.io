<script setup>
import { ref } from 'vue';
let id = 0
const newTodo = ref()
const todos = ref(
    [
        { id: id++, text: 'learn html' },
        { id: id++, text: 'learn javascript' },
        { id: id++, text: 'learn vue' }
    ]
)
function addTodo() {
    todos.value.push({ id: id++, text: newTodo.value })
}
function removeTodo(todo) {
    todos.value = todos.value.filter((x) => x !== todo)
}
</script>
<template>
    <form @submit.prevent='addTodo'>
        <input v-model="newTodo">
        <button>Add Todo</button>
    </form>
    <ul>
        <li v-for="todo in todos" v-bind:key="todo.id">
            <input type="checkbox" v-model="todo.done">
            <span v-bind:class="{ done: todo.done }">{{ todo.text }}</span>
            <button @click="removeTodo(todo)">X</button>
        </li>
    </ul>
</template>
<style>
.done {
    text-decoration: line-through;
}
</style>