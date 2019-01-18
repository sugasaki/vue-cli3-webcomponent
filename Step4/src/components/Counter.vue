<template>
  <div class="hello">
    <h1>{{ count }}</h1>
    <button v-on:click="countUp">Click me</button>
  </div>
</template>

<script>
export default {
  name: "Counter",
  props: {
    count: {
      type: Number,
      default: 0,
      required: true
    }
  },
  data() {
    return {
      count
    };
  },
  methods: {
    /** テキストが入力された時に呼び出される */
    countUp() {
      this.count += 1;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
