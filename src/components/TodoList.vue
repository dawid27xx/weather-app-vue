<template >
    <section class="bg-gray-100 px-10 text-center">
        <h1 class="text-3xl py-5">My To-Do List</h1><hr/><br/>
      <input class="text-left bg-white border rounded-md py-2 w-96 px-2 border-black" type="text" v-model="newTask" @keyup.enter="addTask" placeholder="Describe your task">
      <button class="bg-white hover:bg-blue-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded" @click="addTask">Add Task</button>
      <br /><br /><hr class="border border-gray-500"/><br/>
      <ul>
  <li class="border shadow-md py-4 bg-white border-black rounded-md mb-4 flex justify-between items-center px-4" v-for="(task, index) in tasks" :key="index">
    <span class="flex-1 text-left">{{ task }}</span>
    <button class="bg-white hover:bg-green-700 text-green-700 font-semibold hover:text-white py-1 px-2 border border-gray-500 hover:border-transparent rounded" @click="removeTask(index)">✓</button>
  </li>
    </ul>
    <br /><br/><br /><br />
    </section>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    name: 'TodoList',
    setup() {
      const newTask = ref('');
      const tasks = ref([]);
  
      const addTask = () => {
        if (newTask.value.trim() !== '') {
          tasks.value.push(newTask.value);
          newTask.value = '';
        }
      };
  
      const removeTask = (index) => {
        tasks.value.splice(index, 1);
      };
  
      return { newTask, tasks, addTask, removeTask };
    }
  };
  </script>
  
  <style>
  /* Add your styling here */
  </style>
  