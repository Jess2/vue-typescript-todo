<template>
  <div>
    <label for="todo-input"></label>
    <input id="todo-input" type="text" />
    <button @click="addTodo" type="button">Add</button>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "TodoInput",
  methods: {
    addTodo() {
      console.log("add");
    },
  },
});
</script>

<style scoped></style>
