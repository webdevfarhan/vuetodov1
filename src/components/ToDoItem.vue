<template>
  <p>{{ todo.title }} <button v-on:click="$emit('delete-todo', todo.id)">Delete</button></p>
</template>

<script>
export default {
  name: 'ToDoItem',
  props: ['todo']
};
</script>
