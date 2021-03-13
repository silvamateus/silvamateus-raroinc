<template>
  <main class="blog">
    <h2>Blog</h2>
  </main>
</template>

<script>
import posts from "@/services/posts";
export default {
  data() {
    return { posts: [] };
  },
  created() {
    posts()
      .then(res => res.json())
      .then(res => (this.posts = res))
      .catch(err => console.log(err));
  }
};
</script>

<style></style>
