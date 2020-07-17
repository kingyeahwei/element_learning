<template>
  <div id="app">
    <el-page-header @back="goBack" content="详情页面">
      <template slot="title">title</template>
      <template slot="content">content</template>
    </el-page-header>
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
            goBack() {
                console.log("go back!!")
            }
        }
    }
</script>

<style lang="less">
</style>
