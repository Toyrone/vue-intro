<template>
  <div class="card p-4 text-left">
    <div class="mb-3">
      <label for="email" class="form-label">Todo title</label>
      <input
        v-model="title"
        type="text"
        class="form-control"
        id="email"
        placeholder="Name of Todo"
      />
    </div>
    <div>
      <button
        @click="addTodo"
        class="btn btn-outline-primary"
        :disabled="!title"
        variant="outline-primary"
      >
        Add Todo
      </button>
      <b-button @click="$emit('closeForm')" class="ml-4" variant="danger">Cancel</b-button>
    </div>
  </div>
</template>

<script>
export default {
  name: "AddTodo",
  data() {
    return {
      title: ""
    };
  },
  methods: {
    addTodo() {
      this.$emit("newTodo", this.title);
      this.$emit("closeForm");
    }
  }
};
</script>

<style lang="scss" scoped></style>
