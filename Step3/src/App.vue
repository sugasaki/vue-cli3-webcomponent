<template>
  <div id="app">
    <Counter v-bind:count="count"/>
    <Counter v-bind:count="3"/>
    <Button>Hello</Button>
  </div>
</template>

<script>
import Counter from "./components/Counter.vue";
import Button from "./components/Button.vue";

export default {
  name: "app",
  data: function() {
    return {
      count: 2
    };
  },
  components: {
    Counter,
    Button
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
