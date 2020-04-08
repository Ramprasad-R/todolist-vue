<template>
  <div id="app">
    <Todo v-bind:todos="todos" v-on:del-todo="deleteTodo" />
  </div>
</template>

<script>
import Todo from "./components/Todo";
export default {
  name: "App",
  components: {
    Todo
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "first todo",
          completed: true
        },
        {
          id: 2,
          title: "second todo",
          completed: false
        },
        {
          id: 3,
          title: "third todo",
          completed: false
        }
      ]
    };
  },
  methods: {
    deleteTodo(id) {
      console.log(id);
    }
  }
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
}
</style>
