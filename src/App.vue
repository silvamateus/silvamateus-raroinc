<template>
  <div id="app">
    <top-header />
  </div>
</template>

<script>
import TopHeader from "./components/TopHeader.vue";
export default {
  name: "App",
  components: { TopHeader }
};
</script>

<style>
* {
  font-family: "Roboto", sans-serif;
  box-sizing: border-box;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #323469;
}
</style>
