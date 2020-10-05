<template>
    <div class="flex items-center">
        <input id="taskInputBox" @keyup.enter="addTask" class="flex-1 text-center rounded py-2 outline-none" v-model="task" placeholder="Add a task...">
        <button type="button" class="flex-1 text-center bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none" @click="addTask">Add</button>
    </div>
</template>

<script>
export default {
    name: 'AddTask',

    data() {
        return {
            task: ''
        }
    },

    methods: {
        addTask() {
            document.getElementById("taskInputBox").value = ''
            this.$emit('added', this.task)
        }
    }
}
</script>