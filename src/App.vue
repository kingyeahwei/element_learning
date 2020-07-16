<template>
  <div id="app">
    <el-progress text-inside :stroke-width="26" :percentage="70"></el-progress>
    <el-progress text-inside :stroke-width="24" :percentage="100" status="success"></el-progress>
    <el-progress text-inside :stroke-width="22" :percentage="80" status="warning"></el-progress>
    <el-progress text-inside :stroke-width="20" :percentage="50" status="exception"></el-progress>
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
</style>
