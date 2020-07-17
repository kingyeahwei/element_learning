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
                const h = this.$createElement;
                this.$msgbox({
                    title: "消息",
                    message: h("p", null, [
                        h("span", null, "内容可以是"),
                        h("i", {style: "color: teal"}, "VNode")
                    ]),
                    showCancelButton: true,
                    confirmButtonText: "确定",
                    cancelButtonText: "取消",
                    beforeClose: (action, instance, done) => {
                        if (action == "confirm") {
                            instance.confirmButtonLoading = true;
                            instance.confirmButtonText = "执行中...";
                            setTimeout(() => {
                                done();
                                setTimeout(() => {
                                    instance.confirmButtonLoading = false;
                                }, 300);
                            }, 3000);
                        } else {
                            done();
                        }
                    }
                }).then((action) => {
                    this.$message({
                        type: "info",
                        message: "action:" + action
                    })
                }).catch((action) => {
                    console.log(action)
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
