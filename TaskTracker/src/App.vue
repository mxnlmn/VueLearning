<template>
    <div class = "container">
      <Header title = "Task Tracker"/>
      <Tasks @delete-task = "deleteTask" :tasks = "tasks"/>
    </div>
</template>
<script>
import Header from './components/Header.vue'
import Tasks from './components/Tasks.vue'
export default{
  components: {
    Header,
    Tasks
  },
  data(){
    return{
      tasks:[]
    }
  },
  methods:{
    deleteTask(id){
      if(confirm('Are you sure?')){
        this.tasks = this.tasks.filter((task) => task.id !== id)  
      }
    }
  },
  created(){
    this.tasks = [
    {
      id: 1,  
      text: "todo work 1",
      day: "12/25/2022",
      reminder: true
    },
    {
      id: 2,  
      text: "todo work 2",
      day: "12/25/2022",
      reminder: true
    },
    {
      id: 3,  
      text: "todo work 3",
      day: "12/25/2022",
      reminder: false
    },
    ]
  }
}
</script>


<style scoped>
</style>
