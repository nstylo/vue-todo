<template>
  <TodoList />
</template>

<script>
import TodoList from "./components/TodoList.vue"

export default {
  name: "App",
  components: {
    TodoList
  }
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
  font-size: 26px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
