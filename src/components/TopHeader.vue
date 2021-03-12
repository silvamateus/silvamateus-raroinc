<template>
  <div class="header-top">
    <div class="box">
      <p>Vida toda</p>
      <p>BEM ESTAR</p>
      <p>Solução completas para viver mais e melhor</p>
      <button>Quero uma consultoria</button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.header-top {
  display: flex;
  padding: 2em 2em 0 2em;
  flex-direction: column;
  justify-content: flex-end;
  height: 100vh;
  position: relative;
}
.header-top::before {
  content: " ";
  background: url("https://i.picsum.photos/id/46/650/650.jpg?hmac=DUt9PViAbahIOKRB5yvSnnw2YHVT4-wtybHv504sRmM");
  background-repeat: no-repeat;
  background-size: cover;
  position: absolute;
  height: 100vh;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  z-index: -2;
}
.header-top::after {
  content: " ";
  background-color: rgba(255, 255, 255, 0.37);
  position: absolute;
  height: 100vh;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  z-index: -1;
}
.box {
  border: 2px solid #323469;
  width: 26.8rem;
  padding: 3rem 1.5rem;
  display: flex;
  flex-direction: column;
  font-size: 2.1rem;
  margin-top: 30rem;
  position: absolute;
  bottom: -14rem;
}
.box > p:nth-child(1) {
  font-weight: 300;
}
.box > p:nth-child(2) {
  font-size: 8rem;
  padding-bottom: 6rem;
  word-spacing: 10px;
  margin-left: -7px;
}
.box button {
  margin-top: 6rem;
  background-color: #ff9b23;
  color: #fff;
  padding: 1.5rem 1rem;
  font-size: 2rem;
}
</style>
