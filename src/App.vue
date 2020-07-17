<template>
  <div id="app">
    <div class="wrap" style="height: 500px; width: 100%; border: 1px solid blue;overflow-y: auto">
      <div style="height: 2000px;background: red;"></div>
    </div>
    <el-backtop :bottom="100" :right="100" target=".wrap">
      <div
        style="{
        height: 100%;
        width: 100%;
        background-color: #f2f5f6;
        box-shadow: 0 0 6px rgba(0,0,0, .12);
        text-align: center;
        line-height: 40px;
        color: #1989fa;
      }"
      >
        UP
      </div>
    </el-backtop>
  </div>
</template>

<script>
  export default {
    name: "app",
    data() {
      return {}
    },
    methods: {}
  }
</script>

<style lang="less">
  /*#app {*/
  /*  height: 2000px;*/
  /*}*/
</style>
