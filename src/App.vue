<template>
  <div id="app">
    <!-- <HelloWorld /> -->
    <Projects />
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import Projects from "./components/Projects.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
    Projects,
  },
};
</script>

<style>
#app {
  height: 3000px;
  background-color: rgb(247, 244, 244);
  overflow: hidden;
}
* {
  margin: 0;
  padding: 0;
}
</style>
