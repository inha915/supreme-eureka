<template>
  <div id="app">
    <mainLay />
  </div>
</template>

<script>
import mainLay from "@/views/mainLay.vue";

export default {
  name: "App",
  components: {
    mainLay,
  },
};
</script>

<style>
html,
body {
  height: 100%;
  margin: 0; /* 기본 마진 제거 */
  overflow: hidden; /* 스크롤바 제거 */
}

#app {
  width: 100%;
  height: 100%;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
