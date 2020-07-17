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
                this.$prompt("请输入邮箱", "提示", {
                    confirmButtonText: "确定",
                    cancelButtonText: "取消",
                    inputPattern: /[\w!#$%&'*+/=?^_`{|}~-]+(?:\.[\w!#$%&'*+/=?^_`{|}~-]+)*@(?:[\w](?:[\w-]*[\w])?\.)+[\w](?:[\w-]*[\w])?/,
                    inputErrorMessage: "邮箱格式不正确"
                })
                    .then((value) => {
                        this.$message({
                            type: "success",
                            message: "你的邮箱是: " + value
                        })
                    })
                .catch(() => {
                    this.$message({
                        type: "info",
                        message: "取消输入"
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
