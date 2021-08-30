<template>
  <div>
    <div>
      <div id="header"></div>

      <div id="main-container">
        <h2>Todos</h2>
        <Todos v-bind:todosList="copyTodos"/>
      </div>
    </div>
  </div>
</template>

<script>
/* import Search from './components/Search.vue'
import TodoAdd from './components/TodoAdd.vue' */
import Todos from './components/Todos.vue'

export default {
  name: 'App',
  components: {
   /*  Search, */
    Todos,
   /*  TodoAdd, */
  },
  data(){
    return{
      todos:[
        {
          id: 0,
          title: 'Comprar la cena',
          completed: false,
        },
        {
          id: 1,
          title: 'Lavar ropa',
          completed: true,
        },
        {
          id: 2,
          title: 'Llamar al plomero',
          completed: false,
        },
      ],
      copyTodos:[],
    }
  },
  created(){
    this.copyTodos = [... this.todos]
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
