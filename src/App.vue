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
                this.$alert("<strong>这是<i>HMTL</i>片段</strong>", "HTML片段", {
                    dangerouslyUseHTMLString: true
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
