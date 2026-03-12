
<script setup>
import { ref } from 'vue';
const newTask = ref('');
const tasks = ref([]);
function addTask() {
  if (newTask.value.trim()) {
    tasks.value.push({ text: newTask.value, completed: false });
    newTask.value = '';
  }
}

</script>

<template>
<div class="container">
<h1>TODO List</h1>
<form @submit.prevent="addTask">
<input v-model="newTask" placeholder="Add a new task..." />
<button>Add</button>


<ul>
<li v-for="(task, inndax) in tasks" :key="index">
{{task.text}}
</li>
<ul>
</div>
</template>


