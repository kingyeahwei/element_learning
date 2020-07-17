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
                this.$confirm("检测到未保存的内容,是否在离开页面钱保存修改?", "确认消息", {
                    distinguishCancelAndClose: true,
                    confirmButtonText: "保存",
                    cancelButtonText: "放弃修改"
                })
                .then(() => {
                    this.$message({
                        type: "info",
                        message: "保存修改"
                    })
                })
                .catch((action) => {
                    this.$message({
                        type: "info",
                        message: action == "cancel" ? "放弃保存并离开页面" : "停留在当前页面"
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
