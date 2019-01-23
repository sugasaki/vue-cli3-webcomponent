<template>
  <div>
    <h1>{{ mCount }}</h1>
    <el-button type="primary" icon="el-icon-plus" v-on:click="countUp()">Count Up</el-button>
    <el-button type="danger" icon="el-icon-minus" v-on:click="countDown()">Count Down</el-button>
  </div>
</template>


<style>
/* no need to use CSS Modules or Scoped CSS */
@import "../../node_modules/element-ui/lib/theme-chalk/button.css";
</style>


<script>
import Vue from "vue";
import ElementUI from "element-ui";
Vue.use(ElementUI);

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
      required: true
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

