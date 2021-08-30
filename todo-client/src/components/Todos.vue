<template>
  <div>
    <div v-bind:key="todo.id" v-for="todo in todosList">
      <TodoItem v-bind:todoi="todo"/>
    </div>
  </div>
</template>

<script>
import TodoItem from './TodoItem.vue'

export default {
  name: 'Todos',
  props: ['todosList'],
  components: {TodoItem}
}
</script>

<style>

</style>