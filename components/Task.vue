 <template>
<div class="task">
    <div class="content">{{task.content}}</div>
        <div class="buttons">
        <button>Done</button>
        <button class="delete">Delete</button>
</div>
</div>

 </template>
 
 <script>
 export default {
     name:'task-component',
     props:['task']


 }
 </script>
 
 <style>
 
 </style>