<template>
  <div id="app">
    <el-steps :active="1" simple>
      <el-step title="步骤1" icon="el-icon-edit"></el-step>
      <el-step title="步骤2" icon="el-icon-upload"></el-step>
      <el-step title="步骤3" icon="el-icon-picture"></el-step>
    </el-steps>

    <el-steps :active="1" finish-status="success" simple style="margin-top: 20px;">
      <el-step title="步骤 1"></el-step>
      <el-step title="步骤 2"></el-step>
      <el-step title="步骤 3"></el-step>
    </el-steps>
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
        }
    }
</script>

<style lang="less">
</style>
