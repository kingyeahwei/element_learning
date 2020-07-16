<template>
  <div id="app">
    <el-alert title="成功提示的文案" type="success" effect="dark"></el-alert>
    <el-alert title="消息提示的文案" type="info" effect="dark"></el-alert>
    <el-alert title="警告提示的文案" type="warning" effect="dark"></el-alert>
    <el-alert title="错误提示的文案" type="error" effect="dark"></el-alert>
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
