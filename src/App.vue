<template>
  <div id="app">
    <TopicComponent></TopicComponent>
  </div>
</template>

<script>
import TopicComponent from "./components/TopicComponent";

export default {
  name: "App",
  components: {
    TopicComponent
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
