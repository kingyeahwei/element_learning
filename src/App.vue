<template>
  <div id="app">
    <el-rate v-model="value" show-text :texts="texts"></el-rate>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        value: "",
        texts: ["1", "2", "3", "4", "5"]
      };
    },
    methods: {}
  };
</script>

<style lang="less">
</style>
