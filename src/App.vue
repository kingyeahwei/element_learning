<template>
  <div id="app">
    <el-button plain @click="open">使用HTML片段</el-button>
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
                    title: "html片段",
                    dangerouslyUseHTMLString: true,
                    message: "<strong>这是<i>HTML</i>片段</strong>"
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
