<template>
  <div id="app">
    <el-button :plain="true" @click="openHTML">使用html片段</el-button>
  </div>
</template>

<script>
    export default {
        name: "app",
        data() {
            return {}
        },
        methods: {
            openHTML() {
                this.$message({
                    dangerouslyUseHTMLString: true,
                    message: "<strong>这是<i>HMTL</i>片段</strong>"
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
