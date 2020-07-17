<template>
  <div id="app">
    <el-button plain @click="open">偏移的消息</el-button>
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
                this.$notify({
                    title: "偏移",
                    message: "这是一条带有偏移的提示消息",
                    offset: 300,
                    position: "bottom-right"
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
