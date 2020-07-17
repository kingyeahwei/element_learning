<template>
  <div id="app">
    <el-steps :space="200" :active="1" finish-status="success">
      <el-step title="已完成"></el-step>
      <el-step title="进行中"></el-step>
      <el-step title="步骤3"></el-step>
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
