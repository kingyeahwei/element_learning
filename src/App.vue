<template>
  <div id="app">
    <el-input-number
      v-model="num"
      :disabled="true"
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
