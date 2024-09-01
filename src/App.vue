<template>
  <div id="app" class="bg-gray-500">
    <TodoList />
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue';

export default {
  name: 'App',
  components: {
    TodoList
  }
};
</script>

<style>
/* Ensure the root element covers the viewport */
html, body, #app {
  min-height: 100%;
  margin: 0;
  padding: 0;
}
</style>


