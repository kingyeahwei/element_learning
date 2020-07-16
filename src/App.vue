<template>
  <div id="app">
    <el-alert title="不可关闭的alert" type="success" :closable="false"></el-alert>
    <el-alert title="自定义 close-text" close-text="知道了"></el-alert>
    <el-alert title="设置了回调的alert" type="warning" @close="hello"></el-alert>
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
      hello() {
        alert("hello world");
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
