<template>
  <div id="navbar">
    <router-link to="/">Home</router-link>|
    <router-link to="/about">About</router-link>
  </div>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped>
#navbar {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>