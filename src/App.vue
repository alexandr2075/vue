<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <ul v-for="song in songs" v-bind:key="song">
    <li>{{ song }} kkk</li>
    <li></li>
    <li></li>
    <li></li>
  </ul>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      songs: [],
    };
  },
  components: {},
  mounted() {
    fetch(
      "https://api.spoonacular.com/recipes/complexSearch?apiKey=6521de4893ac4933942e2a9676121c19"
    ).then((response) => (response.results = this.songs));
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
ul {
  width: 300px;
  height: 300px;
  background-color: orange;
}
</style>
