<template>
  <div id="app">
    <el-button type="text" @click="open">点击打开 message box</el-button>
  </div>
</template>

<script>
    export default {
        name: "app",
        data() {
            return {}
        },
        methods: {
            open() {
                this.$confirm("此操作将永久删除该文件, 是否继续?", "提示", {
                    confirmButtonText: "确定",
                    cancelButtonText: "取消",
                    type: "warning",
                    center: true
                })
                .then(() => {
                    this.$message({
                        type: "success",
                        message: "删除成功"
                    })
                })
                .catch(() => {
                    this.$message({
                        type: "info",
                        message: "已经取消删除"
                    })
                })
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
