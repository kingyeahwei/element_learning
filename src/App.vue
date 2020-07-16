<template>
  <div id="app">
    <div class="demo-type">
      <el-avatar :size="60" src="https://empty" @error="errorHandler">
        <img src="https://cube.elemecdn.com/e/fd/0fc7d20532fdaf769a25683617711png.png">
      </el-avatar>
    </div>
  </div>
</template>

<script>
  export default {
    name: "app",
    data() {
      return {
      }
    },
    methods: {
      errorHandler() {
        return true
      }
    }
  }
</script>

<style lang="less">
  .item {
    margin-top: 10px;
    margin-right: 40px;
  }
</style>
