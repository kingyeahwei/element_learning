<template>
  <div id="app"  style="margin: 200px 0 0 200px">
    <el-popconfirm title="这是一段内容确定删除吗?">
      <el-button slot="reference">删除</el-button>
    </el-popconfirm>
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
