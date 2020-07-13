<template>
  <div id="app">
    <el-tooltip :content="'Switch value' + value" placement="top">
      <el-switch
        v-model="value"
        active-color="#13ce66"
        inactive-color="#ff4949"
        active-value="100"
        inactive-value="0"
      ></el-switch>
    </el-tooltip>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        value: "100"
      }
    }
  };
</script>

<style lang="less">
</style>
