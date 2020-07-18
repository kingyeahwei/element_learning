<template>
  <div id="app">
    <el-button @click="drawer = true" type="primary" style="margin-left: 16px;">
      点我打开
    </el-button>

    <el-drawer
      title="我是标题"
      :visible.sync="drawer"
      :with-header="false"
    >
      <span>我来了</span>
    </el-drawer>

  </div>
</template>

<script>
  export default {
    name: "app",
    data() {
      return {
        drawer: false,
      }
    },
    methods: {
    }
  }
</script>

<style lang="less">
</style>
