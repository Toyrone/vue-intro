<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Todo Lists</a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNavDropdown"
          aria-controls="navbarNavDropdown"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
      </div>
    </nav>
    <div class="mt-2">
      <div class="card-body">
        <TodoList :todos="todos" />
      </div>

      <div class="p-4">
        <b-button @click="showForm = true" block variant="primary">Add Todo</b-button>
      </div>

      <AddTodoForm @newTodo="addNewTodo" @closeForm="showForm = false" v-if="showForm" />
    </div>
  </div>
</template>

<script>
import AddTodoForm from "./AddTodoForm";
import TodoList from "./TodoList";

export default {
  name: "TodoWrapper",
  data() {
    return {
      showForm: false,
      todos: [
        {
          id: 1,
          title: "Wake Up",
          isComplete: false
        },
        {
          id: 2,
          title: "Eat",
          isComplete: false
        },
        {
          id: 3,
          title: "Code",
          isComplete: false
        },
        {
          id: 4,
          title: "Rinse and Repeat",
          isComplete: false
        }
      ]
    };
  },
  methods: {
    addNewTodo(payload) {
      const data = {
        id: this.todos.length + 1,
        title: payload,
        inComplete: false
      };

      this.todos.push(data);
    }
  },
  components: {
    AddTodoForm,
    TodoList
  }
};
</script>

<style>
.btn-auto {
  position: absolute;
  right: 10px;
}
</style>
