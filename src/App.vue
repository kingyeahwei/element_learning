<template>
  <div id="app">
    <el-button plain @click="open">隐藏关闭按钮</el-button>
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
                this.$notify.success({
                    title: "info",
                    message: "这是一条没有关闭按钮的消息",
                    showClose: false

                })
            },
        }
    }
</script>

<style lang="less">
  .item {
    margin-top: 10px;
    margin-right: 40px;
  }
</style>
