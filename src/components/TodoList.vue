<template>
  <ul class="list-group">
    <li v-for="todo in todos" :key="todo.id" class="list-group-item text-left relative">
      <input class="mr-2" type="checkbox" name="" id="" />
      {{ todo.title }}
      <button class="btn btn-sm btn-outline-danger btn-auto">Delete</button>
    </li>
  </ul>
</template>

<script>
export default {
  name: "TodoList",
  props: {
    todos: {
      required: true
    }
  },
  data() {
    return {};
  }
};
</script>

<style lang="scss" scoped></style>
