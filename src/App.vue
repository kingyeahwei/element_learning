<template>
  <div id="app">
    <div class="block">
      <el-slider
        v-model="value"
        range
        show-stops
        :max="10"
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
        value: [4, 8]
      }
    },
    methods: {
    }
  };
</script>

<style lang="less">
</style>
