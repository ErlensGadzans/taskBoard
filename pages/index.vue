<template>
<main>
<h1>Task board</h1>
<p>Create a list of tasks</p>
<div class="create-new-task">
  <input 
    type="text" 
    placeholder="Enter new task" 
    v-model="newTask" 
    @keypress.enter="addTask"/>
  <button @click="addTask">Add Task</button>
</div>
<div class="tasks">{{$store.state.tasks}}</div>

</main>
</template>

<script>
export default {
  name: 'IndexPage',
  data(){
    return {
    newTask: ""
    }
  },
  methods:{
    addTask(){
      if(this.newTask){
        this.$store.commit('ADD_TASK', this.newTask);
        this.newTask = '';
      }
    }
  }
}
</script>
