<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" height="100" />
    <h1>Task Manager</h1>
    <TaskList></TaskList>
  </div>
</template>

<script>
import TaskList from './components/TaskList.vue'
export default {
  name: "App",
  components: { TaskList }
};
</script>

<style lang="scss">
@import "./assets/style.scss";
</style>
