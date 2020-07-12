<template>
  <div id="app">
    <el-input-number v-model="num1"></el-input-number>
    <el-input-number v-model="num2" size="medium"></el-input-number>
    <el-input-number v-model="num3" size="small"></el-input-number>
    <el-input-number v-model="num4" size="mini"></el-input-number>
  </div>
</template>

<script>
  export default {
    name: "app",
    data: function () {
      return {
        num1: 1,
        num2: 2,
        num3: 3,
        num4: 4
      };
    },
    methods: {
    }
  };
</script>

<style lang="less">
</style>
