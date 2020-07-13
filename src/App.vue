<template>
  <div id="app">
    <div class="block">
      <span>有默认值</span>
      <el-color-picker
        v-model="color1"
      ></el-color-picker>
    </div>
    <div class="block">
      <span>无默认值</span>
      <el-color-picker
        v-model="color2"
      ></el-color-picker>
    </div>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        color1: "#409eff",
        color2: null
      };
    },
    methods: {}
  };
</script>

<style lang="less">
</style>
