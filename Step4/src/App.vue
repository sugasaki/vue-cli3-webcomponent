<template>
  <div id="app">
    <counter v-bind:count="count"/>
  </div>
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

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
