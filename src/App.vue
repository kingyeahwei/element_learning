<template>
  <div id="app">
    <el-button :plain="true" @click="open">打开消息提示</el-button>
    <el-button :plain="true" @click="openVn">Vnode</el-button>
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
            open() {
                this.$message("这是一条消息提示");
            },
            openVn() {
                const h = this.$createElement;
                this.$message({
                    message: h("p", null, [
                        h("span", null, "内容可以是"),
                        h("i", {style: "color: teal"}, "VNode")
                    ])
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
