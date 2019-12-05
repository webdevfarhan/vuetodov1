<template>
  <div id="app">
    <h1>ToDo App Home</h1>
    <ToDos v-bind:todos="todos" />
  </div>
</template>

<script>
import ToDos from "../components/ToDos";

export default {
  name: "home",
  components: {
    ToDos
  },
  data() {
    return {
      todos: [
        {
          title: "Title 1",
          completed: false,
          id: 1
        },
        {
          title: "Title 2",
          completed: false,
          id: 2
        },
        {
          title: "Title 3",
          completed: false,
          id: 3
        }
      ]
    };
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
