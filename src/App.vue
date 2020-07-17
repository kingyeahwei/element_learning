<template>
  <div id="app">
    <el-button type="text" @click="outerVisible = true">点击打开外层dialog</el-button>

    <el-dialog title="外层dialog" :visible.sync="outerVisible" width="80%">
      <el-dialog
        title="内层dialog"
        width="30%"
        :visible.sync="innerVisible"
        append-to-body
      ></el-dialog>
      <div slot="footer" class="dialog-footer">
        <el-button @click="outerVisible = false">取消</el-button>
        <el-button type="primary" @click="innerVisible = true">打开内层dialog</el-button>
      </div>
    </el-dialog>
  </div>
</template>

<script>
    export default {
        name: "app",
        data() {
            return {
                outerVisible: false,
                innerVisible: false
            }
        },
        methods: {
        }
    }
</script>

<style lang="less">
</style>
