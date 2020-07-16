<template>
  <div id="app">
    <el-alert title="成功提示的文案" type="success" center show-icon></el-alert>
    <el-alert title="消息提示的文案" type="info" center show-icon></el-alert>
    <el-alert title="警告提示的文案" type="warning" center show-icon></el-alert>
    <el-alert title="错误提示的文案" type="error" center show-icon></el-alert>
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
    }
  }
</script>

<style lang="less">
  .item {
    margin-top: 10px;
    margin-right: 40px;
  }
</style>
