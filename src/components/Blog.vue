<template>
  <main class="blog">
    <div class="posts">
      <div v-for="post in posts" :key="post.id" class="post">
        <img
          class="img"
          src="https://i.picsum.photos/id/46/650/650.jpg?hmac=DUt9PViAbahIOKRB5yvSnnw2YHVT4-wtybHv504sRmM"
          alt=""
        />
        <div class="post-text">
          <h3>{{ post.title }}</h3>
          <p>
            {{ post.body }}
          </p>
        </div>
        <div class="btn-container">
          <button>Continuar</button>
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
.blog {
  margin: 0 auto;
  max-width: 1366px;
}
.img {
  width: 100%;
  height: 250px;
  object-fit: cover;
}

/* Posts */
.posts {
  display: flex;
  flex-wrap: wrap;
  align-self: center;
  padding: 1rem 0 1rem 7.2rem;
}
.post {
  border: 2px solid var(--default-bg);
  background-color: var(--default-bg);
  width: 33rem;
  margin: 0 1rem 1rem;
  display: flex;
  flex-direction: column;
}
.post-text {
  background-color: #fff;
  color: var(--default-bg);
  padding: 3rem 1.5rem;
  font-size: 1.2rem;
  overflow: hidden;
  height: 16rem;
}
.post-text p {
  display: -moz-box;
  display: -webkit-box;
  -webkit-line-clamp: 4;
  -webkit-box-orient: vertical;
}
.post-text h3 {
  text-transform: capitalize;
  height: 5rem;
}
.btn-container {
  display: flex;
  justify-content: center;
  padding: 1rem 0 2rem;
}
.btn-container button {
  color: #fff;
  align-self: center;
  background-color: #ff9b23;
  padding: 1rem 1.5rem;
  border-radius: 16px;
}
@media (max-width: 1250px) {
  .title {
    width: 100%;
  }
  .post {
    margin: 1rem auto;
  }
}
@media (max-width: 998px) {
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
