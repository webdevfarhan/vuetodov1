<template>
  <p>{{todo.title}}</p>
</template>

<script>
export default {
  name: "ToDoItem",
  props: ["todo"]
};
</script>

