<template>
  <div id="view">
    <link href="https://fonts.googleapis.com/css2?family=Mukta:wght@500&display=swap" rel="stylesheet">
    <div id="title">
      <h3>Vue ToDo</h3>
    </div>
    <div id="tasks">
      <Task />
    </div>
  </div>
</template>

<script>
import Task from './components/Task.vue'

export default {
  name: 'App',
  components: {
    Task
  }
}
</script>

<style>
* {
  font-family: 'Mukta', sans-serif;
}
</style>