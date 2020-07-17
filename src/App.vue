<template>
  <div id="app">
    <el-steps :active="2" align-center finish-status="error">
      <el-step title="步骤1" description="走上社会发斯蒂芬斯蒂芬地方"></el-step>
      <el-step title="步骤2" description="走上社会发斯蒂芬斯蒂芬地方"></el-step>
      <el-step title="步骤3" description="走上社会发斯蒂芬斯蒂芬地方"></el-step>
      <el-step title="步骤4" description="走上社会发斯蒂芬斯蒂芬地方"></el-step>
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
