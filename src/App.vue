<template>
  <div id="app">
    <el-input-number
      v-model="num"
      :precision="2"
      :step="0.1"
      :max="10"
    ></el-input-number>
  </div>
</template>

<script>
  export default {
    name: "app",
    data: function () {
      return {
        num: 1
      };
    },
    methods: {
    }
  };
</script>

<style lang="less">
</style>
