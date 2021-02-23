<template>
  <div>
    <p>Testimonial Page</p>
    <HelloWorld :msg="message" />
  </div>
</template>

<script>
import HelloWorld from "../components/HelloWorld.vue";

export default {
  name: "TestimonialPage",
  data() {
    return {
      message: "Welcome to Your Testimonials page"
    };
  },
  components: {
    HelloWorld
  }
};
</script>
