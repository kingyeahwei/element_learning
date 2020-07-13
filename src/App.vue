<template>
  <div id="app">
    <el-switch
      v-model="value1"
      disabled
    ></el-switch>
    <el-switch
      v-model="value2"
      disabled
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
        value2: false
      }
    }
  };
</script>

<style lang="less">
</style>
