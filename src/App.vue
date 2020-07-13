<template>
  <div id="app">
    <div class="block">
      <span class="demostration">不显示间隔点</span>
      <el-slider
        v-model="value1"
        :step="10"
      ></el-slider>
    </div>
    <div class="block">
      <span class="demostration">显示间隔点</span>
      <el-slider
        v-model="value2"
        :step="10"
        show-stops
      ></el-slider>
    </div>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        value1: 0,
        value2: 0,
      }
    },
    methods: {
    }
  };
</script>

<style lang="less">
</style>
