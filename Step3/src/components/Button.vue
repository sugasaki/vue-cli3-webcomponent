<template>
  <div>
    <el-button icon="el-icon-search" circle></el-button>

    <el-button type="primary" v-on:click="onClick()">
      <slot>{{ msg }}</slot>
    </el-button>
  </div>
</template>

<script>
export default {
  name: "button",
  props: {
    msg: String
  },
  methods: {
    onClick() {
      this.$emit("click");
    }
  }
};
</script>


<style scoped>
/* no need to use CSS Modules or Scoped CSS */
@import "../../node_modules/element-ui/lib/theme-chalk/button.css";
</style>
