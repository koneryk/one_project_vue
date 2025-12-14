<script setup>
import { ref } from 'vue';

const createTaskRef = ref(null); 
const taskWrapperRef = ref(null); 

const mainStyle = "display:flex;";
const hideStyle = "display:none;";

const currentStyle = ref(mainStyle); 

const tasks = ref([]);

function handleToggle() {
  currentStyle.value = currentStyle.value === mainStyle ? hideStyle : mainStyle;
  createTaskRef.value.style = currentStyle.value;
}

function addTask() {
  const taskInput = createTaskRef.value.querySelector('.task-input');
  if (taskInput && taskInput.value.trim() !== "") {
    tasks.value.push(taskInput.value);
    taskInput.value = "";
  }
}
</script>

<template>
  <button @click="handleToggle">
    {{ currentStyle === mainStyle ? 'Скрыть форму' : 'Показать форму' }}
  </button>
  <div ref="createTaskRef" :style="{ display: currentStyle === mainStyle ? 'flex' : 'none' }" class="create-task">
    <input type="text" class="task-input" placeholder="Новая задача" />
    <button @click="addTask">Добавить задачу</button>
  </div>
  
  <ul ref="taskWrapperRef" class="task-list">
    <li v-for="(task) in tasks" >{{ task }}</li>
  </ul>
</template>

<style scoped>
.create-task {
  margin-top: 10px;
  gap: 10px;
  align-items: center;
}
.task-list {
  margin-top: 20px;
  list-style-type: disc;
  padding-left: 20px;
}
</style>