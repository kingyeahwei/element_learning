<template>
  <div id="app">
    <el-button type="text" @click="open">点击打开messagebox</el-button>
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
                this.$alert("这是一段内容", "标题内容", {
                    confirmButtonText: "确定",
                    callback: (action) => {
                        this.$message({
                            type: "info",
                            message: `action: ${action}`
                        })
                    }
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
