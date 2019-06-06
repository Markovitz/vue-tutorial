<template>
  <div v-bind:class="classObject">
    <h1>Topic component {{ name }}</h1>
  </div>
</template>

<script>
export default {
  name: "TopicComponent",
  props: {
    msg: String
  },
  data() {
    return {
      name: "Markovitz",
      isActive: true,
      //error: null
      error: {
        type: "fatal"
      }
    };
  },
  computed: {
    classObject: function() {
      return {
        active: this.isActive && !this.error,
        "text-danger": this.error && this.error.type === "fatal"
      };
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.active {
  text-decoration: underline;
}
.text-danger {
  color: red;
}

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
