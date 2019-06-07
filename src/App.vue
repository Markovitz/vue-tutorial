<template>
  <div id="app">
    <TopicComponent></TopicComponent>
    <h1>Main Window</h1>
    <ul>
      <li :key="requirement.id" v-for="requirement in requirements" class="requirement">
        <p>{{ requirement.lang }}</p>
        <p>{{ requirement.level }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
import TopicComponent from "./components/TopicComponent";

export default {
  name: "App",
  components: {
    TopicComponent
  },
  data() {
    return {
      requirements: [
        {
          id: 1,
          lang: "Java",
          level: "Medium"
        },
        {
          id: 2,
          lang: "Cpp",
          level: "High"
        },
        {
          id: 3,
          lang: "Phyton",
          level: "Low"
        },
        {
          id: 4,
          lang: "Spring",
          level: "Very High"
        }
      ]
    };
  }
};
</script>

<style scoped>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1 {
  color: #1548b6;
}
.requirement {
  background: #eee;
  text-align: left;
  padding: 5px;
  margin-bottom: 20px;
  list-style: none;
}
p:first-child {
  font-weight: bold;
}
p:last-child {
  font-size: 2em;
}
</style>
