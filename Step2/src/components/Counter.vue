<template>
  <v-app>
    <h1>{{ count }}</h1>
    <v-btn color="success" v-on:click="countUp">Count Up</v-btn>
    <v-btn color="info" v-on:click="countDown">Count Down</v-btn>
  </v-app>
</template>


<style>
/* no need to use CSS Modules or Scoped CSS */
@import "../../node_modules/vuetify/dist/vuetify.min.css";
</style>


<script>
import Vue from "vue";
import Vuetify from "vuetify";
Vue.use(Vuetify);

export default {
  name: "Counter",
  props: {
    count: {
      type: Number,
      default: 0,
      required: true
    }
  },
  methods: {
    countUp() {
      this.count += 1;
    },
    countDown() {
      this.count -= 1;
    }
  }
};
</script>

