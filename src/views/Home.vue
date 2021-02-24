<!-- eslint-disable -->
<template>
  <div class="home">
    <div class="home-wrapper">
      <TodoWrapper />
    </div>
  </div>
</template>

<script>
import TodoWrapper from "../components/TodoWrapper";

export default {
  name: "Home",
  components: {
    TodoWrapper
  }
};
</script>

<style scoped>
.home-wrapper {
  max-width: 500px;
  margin: 0 auto;
}
</style>
