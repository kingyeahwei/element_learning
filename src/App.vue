<template>
  <div id="app">
    <el-switch v-model="value" active-color="#13ce66" inactive-color="#ff4949"></el-switch>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        value: true
      }
    }
  };
</script>

<style lang="less">
</style>
