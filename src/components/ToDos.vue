<template>
  <div class="flexContainer">
    <div v-bind:key="todo.id" v-for="todo in todos">
      <ToDoItem v-bind:todo="todo" />
    </div>
  </div>
</template>

<script>
import ToDoItem from '../components/ToDoItem';
export default {
  name: 'ToDos',
  components: {
    ToDoItem
  },
  props: ['todos']
};
</script>
