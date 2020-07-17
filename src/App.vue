<template>
  <div id="app">
    <el-button :plain="true" @click="open2">成功</el-button>
    <el-button :plain="true" @click="open3">警告</el-button>
    <el-button :plain="true" @click="open1">消息</el-button>
    <el-button :plain="true" @click="open4">错误</el-button>
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
            open1() {
                this.$message.info("这是一条消息提示");
            },
            open2() {
                this.$message({
                    message: "恭喜你,这是一条成功消息",
                    type: "success"
                })
            },
            open3() {
                this.$message({
                    message: "警告偶,这是一条警告消息",
                    type: "warning"
                })
            },
            open4() {
                this.$message.error("错了,这是一条错误消息")
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
