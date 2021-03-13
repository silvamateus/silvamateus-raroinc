<template>
  <main class="blog">
    <div class="title">
      <h2>Blog</h2>
    </div>
    <div class="posts">
      <div v-for="post in posts" :key="post.userid" class="post">
        <img
          width="100%"
          height="250px"
          src="https://i.picsum.photos/id/46/650/650.jpg?hmac=DUt9PViAbahIOKRB5yvSnnw2YHVT4-wtybHv504sRmM"
          alt=""
        />
        <div class="post-text">
          <h3>{{ post.title }}</h3>
        </div>
      </div>
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
  margin: 2rem;
}
.post-text {
  background-color: #fff;
  color: var(--default-bg);
  padding: 3rem 1.5rem;
}
.post-text h3 {
  text-transform: capitalize;
}
@media (max-width: 998px) {
  .title {
    width: 100%;
  }
  .posts {
    margin-left: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .post {
    margin: 2rem 0;
    width: 100%;
  }
}
</style>
