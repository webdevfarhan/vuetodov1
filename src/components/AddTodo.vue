<template>
  <form @submit="addTodo">
    <input type="text" placeholder="Add New Todo" name="title" v-model="title" />
    <input type="submit" value="Submit" />
  </form>
</template>

<script>
import uuid from 'uuid';
export default {
  name: 'AddTodo',
  data() {
    return {
      title: ''
    };
  },
  methods: {
    addTodo(e) {
      const newTodo = {
        title: this.title,
        completed: false,
        id: uuid.v4()
      };
      e.preventDefault();
      this.$emit('add-todo', newTodo);
      this.title = '';
    }
  }
};
</script>
