<template>
  <section class="s-notFound">
    <h2>Page not found</h2>
    <h4>This page could not be found 404</h4>
    <router-link to="/posts">Go back to Posts</router-link>
  </section>
</template>
<script>
export default {
  name: "NotFound",
  props: {
    message: {
      type: String,
      required: true,
      default: "Hello",
      validator: function (value) {
        return value !== "";
      },
    },
  },
  created() {
    // LOg component name
    console.log(this.message + this.$options.name);
  },
};
</script>
