<template>
  <main class="blog">
    <div class="title">
      <h2>Blog</h2>
    </div>
    <div class="posts">
      <div v-for="post in posts" :key="post.userid" class="post"></div>
    </div>
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

<style scoped>
/* Blog */

/* Title */
.title {
  background-color: var(--default-bg);
  color: #fff;
  width: 590px;
  padding: 2rem;
  font-size: 3rem;
  text-align: center;
  margin-bottom: 3rem;
}

/* Posts */
.posts {
  display: flex;
  flex-wrap: wrap;
  margin-left: 7.1rem;
}
.post {
  border: 2px solid var(--default-bg);
  background-color: var(--default-bg);
  width: 29rem;
  padding: 2rem;
  margin: 1rem;
}
</style>
