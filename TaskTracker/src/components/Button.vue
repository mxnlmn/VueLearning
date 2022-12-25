<script>
export default {
    name: "Button",
    props:['buttonText'],
    methods:{
        onClick(){
            console.log("click")
        }
    }
}
</script>
<template>
    <div>
        <button @click = "onClick()">Add Task</button>
    </div>
</template>