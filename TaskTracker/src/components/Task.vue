<template>
    <div :class = "[task.reminder ? 'reminder' : '', 'task']">
        <h3>{{task.text}}</h3>
            <p>{{task.day}}</p>
            <button @click = "deleteTask(task.id)">Delete Task</button>
    </div>
</template>
<script>
export default {
    name:'Task',
    props:{
        task: Object
    },
    methods:{
        deleteTask(id){
            this.$emit('delete-task', id)
            // console.log(id)
        }
    }

}
</script>
<style scope>

</style>>
