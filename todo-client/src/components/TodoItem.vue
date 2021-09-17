<template>
  <div class="todo"  v-bind:class="{completed: todoi.completed}">
    <div class="todo-body">
      <input type="checkbox"  v-bind:checked="todoi.completed ? 'checked': none">
      {{ todoi.title }}
    </div>
    <div class="todo-actions">
      <button>Delete</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TodoItem',
  props:['todoi'],
}
</script>

<style>

</style>