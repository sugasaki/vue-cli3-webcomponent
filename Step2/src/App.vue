<template>
  <v-app>
    <div id="app">
      <h1>{{ count }}</h1>

      <Counter v-bind:count="count"/>
      <Counter v-bind:count="3"/>
    </div>
  </v-app>
</template>

<script>
import Counter from "./components/Counter.vue";

export default {
  name: "app",
  data: function() {
    return {
      count: 2
    };
  },
  components: {
    Counter
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
