<template>
  <div>
    <p>Testimonial Page</p>
    <HelloWorld @updateMessage="handleMessageUpdate" :msg="message" />
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
  methods: {
    handleMessageUpdate(payload) {
      this.message = payload.msg;
    }
  },
  components: {
    HelloWorld
  }
};
</script>
