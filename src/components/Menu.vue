<template>
  <div class="menu">
   <h2 class="menu-header">hello vuejs</h2>

   <input type="text" v-model = "name"/>{{name}}

   <input type ="checkbox" @click ="hide = ! hide"/> Hide
   <h2  v-show = "hide" v-bind:id="id">phung vip pro</h2>

    <h2 class="" v-bind:class = "{changeColor: changed}">doi mau text nay nha</h2>
    <button class="" @click = "changed = !changed">Doi mau</button>
  </div>

  <input type="text" v-model = "newTask"/>
  <button class="" @click = "addTask()">Add todo</button>
  
  <div v-for ="(task, index) in tasks" :key="index">
      <input type="checkbox" v-model="task.done"/>
      <span :class="{done: task.done}">{{task.todo}}</span>
      
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      name: "van duc",
      hide: true,
      id: 'abc',
      changed: true,
      tasks: [
        {
          todo:  'code', done: false,
        },
        {
          todo:   "workout", done: false,
        },
        {
          todo:  'sleep', done: false,
        },
        {
          todo:  'cook', done: false,
        }    
        
      ],
      newTask : '',
     
    }
  },
   methods : {
      addTask: function() {
          this.tasks.push(
            {todo: this.newTask, done: false}
            )
        }
   },
   watch: {
     newTask: function() {
       console.log('new task changed')
     }
   }
}
</script>


<style scoped>
  .menu-header {
    color: rgb(100,100,100);
  }
  .changeColor {
    color: red;
  }
  .done {
    text-decoration: line-through;
  }
</style>
