<template>
  <div id="app">
    <el-color-picker
      v-model="color"
      show-alpha
    ></el-color-picker>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        color: "rgba(19, 206, 102, 0.8)",
      };
    },
    methods: {}
  };
</script>

<style lang="less">
</style>
