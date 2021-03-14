<template>
  <div id="app">
    <div class="header-background">
      <top-header />
    </div>
    <div class="title">
      <h2>Blog</h2>
    </div>
    <blog />
  </div>
</template>

<script>
import Blog from "./components/Blog.vue";
import TopHeader from "./components/TopHeader.vue";
export default {
  name: "App",
  components: { TopHeader, Blog }
};
</script>

<style>
:root {
  --header-height: 670px;
  --default-bg: #323469;
}
.title {
  background-color: var(--default-bg);
  color: #fff;
  width: calc(50% - 1.9rem);
  padding: 2rem;
  font-size: 3rem;
  text-align: center;
  margin-bottom: 3rem;
}
* {
  font-family: "Roboto", sans-serif;
  box-sizing: border-box;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #323469;
}

.header-background::before {
  content: " ";
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background: url("https://i.picsum.photos/id/46/650/650.jpg?hmac=DUt9PViAbahIOKRB5yvSnnw2YHVT4-wtybHv504sRmM");
  background-color: rgba(255, 255, 255, 0.37);
  background-repeat: no-repeat;
  background-size: cover;
  height: var(--header-height);
  z-index: -2;
}
.header-background::after {
  content: " ";
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(255, 255, 255, 0.308);
  height: var(--header-height);
  z-index: -1;
}
</style>
