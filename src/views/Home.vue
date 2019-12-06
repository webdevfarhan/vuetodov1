<template>
  <div id="app">
    <h1>ToDo App Home</h1>
    <AddTodo v-on:add-todo="addTodo" />
    <ToDos v-bind:todos="todos" />
  </div>
</template>

<script>
import ToDos from '../components/ToDos';
import AddTodo from '../components/AddTodo';

export default {
  name: 'home',
  components: {
    ToDos,
    AddTodo
  },
  data() {
    return {
      todos: [
        {
          title: 'Title 1',
          completed: false,
          id: 1
        },
        {
          title: 'Title 2',
          completed: false,
          id: 2
        },
        {
          title: 'Title 3',
          completed: false,
          id: 3
        }
      ]
    };
  },
  methods: {
    addTodo(newTodo) {
      this.todos = [...this.todos, newTodo];
    }
  }
};
</script>

<style scoped>
#app {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
