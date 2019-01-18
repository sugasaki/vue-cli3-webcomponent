<template>
  <v-app>
    <h1>{{ count }}</h1>
    <el-button type="primary" icon="el-icon-search" v-on:click="countUp()">Count Up</el-button>
    <el-button type="danger" icon="el-icon-search" v-on:click="countDown()">Count Down</el-button>
  </v-app>
</template>


<style>
/* no need to use CSS Modules or Scoped CSS */
@import "../../node_modules/element-ui/lib/theme-chalk/index.css";
</style>


<script>
import Vue from "vue";
import ElementUI from "element-ui";
Vue.use(ElementUI);

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

