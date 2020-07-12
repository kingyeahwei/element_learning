<template>
  <div id="app">
    <el-input-number
      v-model="num"
      :step="2"
      :step-strictly="true"
    ></el-input-number>
  </div>
</template>

<script>
  export default {
    name: "app",
    data: function () {
      return {
        num: 5
      };
    },
    methods: {
    }
  };
</script>

<style lang="less">
</style>
