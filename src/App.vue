<template>
  <div id="app"  style="margin: 200px 0 0 200px">
    <el-popconfirm
      confirm-button-text="好的"
      cancel-button-text="不用了"
      icon="el-icon-search"
      iconColor="green"
      title="这是一段内容确定删除吗?"
      @onConfirm="handleConfirm"
      @onCancel="handleCancel"
    >
      <el-button slot="reference">删除</el-button>
    </el-popconfirm>
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
            handleConfirm() {
                alert("确定")
            }
            ,
            handleCancel() {
                alert("取消")
            }
        }
    }
</script>

<style lang="less">
</style>
