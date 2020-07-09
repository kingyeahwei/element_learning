<template>
  <div id="app">
    <el-link href="http://www.baidu.com" target="_blank" icon="el-icon-edit">默认链接</el-link>
    <el-link type="primary" icon="el-icon-share">主要链接</el-link>
    <el-link type="success" :underline="false">成功链接</el-link>
    <el-link type="warning" :underline="false">警告链接</el-link>
    <el-link type="danger" :underline="false">危险链接</el-link>
  </div>
</template>

<script>
  export default {};
</script>

<style lang="less">
</style>
