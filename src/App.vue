<template>
  <div id="app">
    <div class="block">
      <span>默认不区分颜色</span>
      <el-rate v-model="value1"></el-rate>
    </div>
    <div class="block">
      <span>区分颜色</span>
      <el-rate v-model="value2" :colors="colors"></el-rate>
    </div>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        value1: null,
        value2: null,
        colors: ["#99a9bf", "#f7ba2a", "#ff9900"]
      };
    },
    methods: {}
  };
</script>

<style lang="less">
</style>
