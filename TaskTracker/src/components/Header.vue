<template>
    <div class = "header">
        <h1>{{ title }}</h1>
        <Button />
    </div>
</template>
<script>
import Button from './Button.vue'
export default {
    name: "Header",
    props:['title'],
    components:{
        Button
    }
}
</script>