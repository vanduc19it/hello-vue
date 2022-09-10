<template> 
  <Menu/>
  <Content/>
  <Task v-for ="(task, index) in tasks" :key="index" :taskData='task'/>
  <Footer/>
  <TagSelector/>
  <hr/>
  <Fillter/>
 
</template>

<script>

import Menu from './components/Menu.vue'
import Content from './components/Content.vue'
import Footer from './components/Footer.vue'
import Task from './components/Task.vue'
import TagSelector from './components/TagSelector.vue'
import Fillter from './components/Fillter.vue'
export default {
  name: 'App',
  components: {
    Menu,
    Content,
    Task,
    TagSelector,
    Footer,
    Fillter,
  },
  data() {
    return {
      tasks : [
        {todo: 'code', done: false },
        {todo: 'ngu', done: false },
        {todo: 'an', done: false },
        {todo: 'luotfb', done: false }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
