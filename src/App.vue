<template>
  <div id="app">
    <div class="block">
      <el-slider
        v-model="value"
        vertical
        height="200px"
      ></el-slider>
    </div>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        value: 0
      }
    },
    methods: {
    }
  };
</script>

<style lang="less">
</style>
