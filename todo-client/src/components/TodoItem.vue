<template>
  <div>
    <div class="todo-body">
      <input type="checkbox">
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