<template class="todo-item">
  <li :style="style">
    {{ msg }}
  </li>
</template>

<script>
export default {
  name: "TodoItem",
  props: {
    msg: String,
    isDone: Boolean
  },
  data: function() {
    return {
      style: {
        backgroundColor: this.isDone ? "grey" : "white"
      }
    }
  }
}
</script>

<style scoped>
li {
  list-style-type: none;
  width: auto;
  min-height: 2em;
  margin: 10px 0;
}
</style>
