<template>
  <div id="app">
    <div class="header-background">
      <top-header />
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
}
</style>
