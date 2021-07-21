<template>
  <div>
    <h1>Vue Todo with TypeScript</h1>
    <TodoInput :item="todoText" @input="updateTodoText" @add="addTodoItem" />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import TodoInput from "@/components/TodoInput.vue";

export default Vue.extend({
  data() {
    return {
      todoText: "",
    };
  },
  methods: {
    updateTodoText(value: string) {
      this.todoText = value;
    },
    addTodoItem() {
      const value = this.todoText;
      localStorage.setItem(value, value);
      this.initTodoText();
    },
    initTodoText() {
      this.todoText = "";
    },
  },
  components: { TodoInput },
});
</script>

<style scoped></style>
