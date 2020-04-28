<template class="todo-item">
  <li>
    {{ msg }}
  </li>
</template>

<script>
export default {
  name: "TodoItem",
  props: ["msg"]
};
</script>

<style scoped>
li {
  list-style-type: none;
}
</style>
