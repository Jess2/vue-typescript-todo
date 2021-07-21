<template>
  <div>
    <h1>Vue Todo with TypeScript</h1>
    <TodoInput :item="todoText" @input="updateTodoText" />
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
    updateTodoText(value: any) {
      this.todoText = value;
    },
  },
  components: { TodoInput },
});
</script>

<style scoped></style>
