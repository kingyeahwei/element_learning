<template>
  <div id="app">
    <el-switch v-model="value1" active-text="按月付费" inactive-text="按年付费"></el-switch>
    <el-switch
      v-model="value2"
      active-color="#13ce66"
      inactive-color="#ff4949"
      active-text="按月付费"
      inactive-text="按年付费"
    ></el-switch>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        value1: true,
        value2: true
      }
    }
  };
</script>

<style lang="less">
</style>
