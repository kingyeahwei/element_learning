<template>
  <div id="app">
    <el-steps :active="active" finish-status="success">
      <el-step title="步骤1"></el-step>
      <el-step title="步骤2"></el-step>
      <el-step title="步骤3"></el-step>
      <el-step title="步骤4"></el-step>
    </el-steps>
    <el-button style="margin-top: 12px" @click="next">下一步</el-button>
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
            next() {
                if (this.active++ > 3) {
                    this.active = 0;
                }
            }
        }
    }
</script>

<style lang="less">
</style>
