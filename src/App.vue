<template>
  <div id="app">
    <el-steps :active="1">
      <el-step title="步骤1" icon="el-icon-edit"></el-step>
      <el-step title="步骤2" icon="el-icon-upload"></el-step>
      <el-step title="步骤3" icon="el-icon-picture"></el-step>
    </el-steps>
  </div>
</template>

<script>
    export default {
        name: "app",
        data() {
            return {
                active: 1
            }
        },
        methods: {
        }
    }
</script>

<style lang="less">
</style>
