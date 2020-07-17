<template>
  <div id="app">
    <div style="height: 300px">
      <el-steps :active="1" direction="vertical">
        <el-step title="步骤1" icon="el-icon-edit"></el-step>
        <el-step title="步骤2" icon="el-icon-upload"></el-step>
        <el-step title="步骤3" icon="el-icon-picture"></el-step>
      </el-steps>
    </div>
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
