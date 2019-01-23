<template>
  <div>
    <h1>{{ mCount }}</h1>
    <v-btn color="success" v-on:click="countUp">Count Up</v-btn>
    <v-btn color="info" v-on:click="countDown">Count Down</v-btn>
  </div>
</template>


<style scoped>
/* no need to use CSS Modules or Scoped CSS */
@import "../../node_modules/vuetify/dist/vuetify.min.css";
</style>


<script>
import Vue from "vue";
import Vuetify from "vuetify";
Vue.use(Vuetify);

export default {
  name: "Counter",
  data: function() {
    return {
      mCount: 0
    };
  },
  props: {
    count: {
      type: Number,
      default: 0,
      required: false
    }
  },
  created() {
    this.mCount = this.count;
  },
  async mount() {},
  methods: {
    countUp() {
      this.mCount += 1;
    },
    countDown() {
      this.mCount -= 1;
    }
  }
};
</script>

