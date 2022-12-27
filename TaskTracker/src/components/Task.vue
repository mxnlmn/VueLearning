<template>
    <div @dblclick="$emit('toggle-reminder', task.id)" :class = "[task.reminder ? 'reminder' : '', 'task']">
        <h3>{{task.text}}</h3>
        <p>{{task.day}}</p>
        <button @click = "$emit('delete-task', task.id)">Delete Task</button>
    </div>
</template>
<script>
export default {
    name:'Task',
    props:{
        task: Object
    },

}
</script>
<style scope>

</style>>
