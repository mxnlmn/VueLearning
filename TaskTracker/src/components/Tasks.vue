<template>
    <div :key="task.id" v-for = "task in tasks" class="tasksContainer">
        <Task @delete-task = "$emit('delete-task', task.id)" :task = "task"/>
    </div>
</template>
<script>
import Task from './Task.vue'
export default {
    name:"Tasks",
    props:{
        tasks: Array
    },
    components:{
        Task
    },
    emits:['delete-task']
}
</script>