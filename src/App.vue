<template>
  <div id="app">
    <el-color-picker v-model="color"></el-color-picker>
    <el-color-picker v-model="color" size="medium"></el-color-picker>
    <el-color-picker v-model="color" size="small"></el-color-picker>
    <el-color-picker v-model="color" size="mini"></el-color-picker>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        color: '#409eff',
      };
    },
    methods: {}
  };
</script>

<style lang="less">
</style>
