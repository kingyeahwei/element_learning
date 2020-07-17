<template>
  <div id="app">
    <el-button :plain="true" @click="openCenter">文字居中</el-button>
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
            openCenter() {
                this.$message({
                    message: "居中的文字",
                    center: true
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
