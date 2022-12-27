<template>
    <div class = "container">
      <Header title = "Task Tracker"/>
      <Tasks  @toggle-reminder="toggleReminder" @delete-task = "deleteTask" :tasks = "tasks"/>
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
    },
    toggleReminder(id){
      console.log(id)
    }
  },
  created(){
    this.tasks = [
    {
      id: 1,  
      text: "Hi, this is ToDo App",
      day: "12/25/2022",
      reminder: true
    },
    {
      id: 2,  
      text: "This app was made by me with VueJs",
      day: "12/25/2022",
      reminder: true
    },
    {
      id: 3,  
      text: "Enjoy",
      day: "12/25/2022",
      reminder: false
    },
    ]
  }
}
</script>