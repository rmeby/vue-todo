<template>
  <div class="bg-gray-200 flex flex-col h-screen">
    <link href="https://fonts.googleapis.com/css2?family=Mukta:wght@500&display=swap" rel="stylesheet">

    <!-- Display logo -->
    <div class="flex items-center justify-center p-4 text-xl">
      <span>📃 Vue TODO</span>
    </div>

    <!-- Task add input -->
    <div class="flex items-center justify-center p-4">
      <AddTask @added="addTask"/>
    </div>

    <!-- Display tasks -->
    <div class="flex items-center justify-center p-4">
      <ul>
        <li v-for="task in taskList" :key="task">
          <input type="checkbox">
          <label for="checkbox"> {{ task }}</label>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import AddTask from '@/components/AddTask.vue'

export default {
  name: 'App',
  
  components: { AddTask },

  data() {
    return {
      taskList: []
    }
  },

  methods: {
    addTask(task) {
      this.taskList.push(task)
    }
  }
}
</script>

<style>
p {
  font-family: 'Mukta', sans-serif;
}
</style>