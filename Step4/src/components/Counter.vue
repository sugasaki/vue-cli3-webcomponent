<template>
  <div>
    <h1>{{ mCount }}</h1>
    <button v-on:click="countUp">
      <icon-base width="30" height="30" icon-name="plus">
        <icon-plus/>
      </icon-base>
    </button>
    <button v-on:click="countDown">
      <icon-base width="30" height="30" icon-name="minus">
        <icon-minus/>
      </icon-base>
    </button>
  </div>
</template>


<style>
/* no need to use CSS Modules or Scoped CSS */
</style>


<script>
import IconBase from ".//IconBase.vue";
import IconPlus from "./icons/IconPlus.vue";
import IconMinus from "./icons/IconMinus.vue";

export default {
  name: "Counter",
  data: function() {
    return {
      mCount: 0
    };
  },
  components: {
    IconBase,
    IconPlus,
    IconMinus
  },
  props: {
    count: {
      type: Number,
      default: 0,
      required: true
    }
  },
  created() {},
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

