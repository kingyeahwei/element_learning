<template>
  <div id="app">
    <el-button type="text" @click="centerDialogVisible = true">点击打开dialog</el-button>
    <el-dialog
      title="提示"
      :visible.sync="centerDialogVisible"
      width="30%"
      center>
      <div style="text-align: center">
        <span>需要注意的是内容是默认不居中的</span>
      </div>
      <span slot="footer" class="dialog-footer">
        <el-button @click="centerDialogVisible = false">取消</el-button>
        <el-button type="primary" @click="centerDialogVisible = false">确定</el-button>
      </span>
    </el-dialog>
  </div>
</template>

<script>
    export default {
        name: "app",
        data() {
            return {
                centerDialogVisible: false
            }
        },
        methods: {
        }
    }
</script>

<style lang="less">
</style>
