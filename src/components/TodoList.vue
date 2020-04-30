<template id="todo-list">
  <div class="global-wrapper">
    <div class="list-wrapper">
      <header class="list-header">
        Vue Todo App
      </header>
      <input
        class="list-input"
        type="text"
        v-on:keyup.enter="addItem(value)"
        v-model="value"
      />
      <ul class="list">
        <TodoItem
          class="list-item"
          v-for="item in todos"
          :key="item.id"
          :msg="item.text"
        />
      </ul>
    </div>
  </div>
</template>

<script>
import TodoItem from "./TodoItem"

export default {
  name: "TodoList",
  data: function() {
    return {
      value: "",
      todos: [],
      id: 0
    }
  },
  methods: {
    addItem: function(text) {
      this.value = ""
      this.todos.push({ text: text, id: this.id++ }) // TODO: might use different function
    }
  },
  components: {
    TodoItem
  }
}
</script>

<style scoped>
.global-wrapper {
  height: 100vh;
  width: 100%;
  display: flex;
  justify-content: center;
  margin-top: 80px;
}

.list-wrapper {
  width: 14em;
  display: flex;
  flex-direction: column;
}

.list {
  padding-inline-start: 0;
}

.list-input {
  height: 1.4em;
  font-size: 1em;
  width: auto;
  padding: 0 10px;
}

.list-header {
  text-align: center;
  margin-bottom: 30px;
}
</style>
