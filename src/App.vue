<template>
  <div id="app">
    <el-steps :active="1">
      <el-step title="步骤1" description="这是一段很长很长很长的描述性文字这是一段很长很长很长的描述性文字"></el-step>
      <el-step title="步骤2" description="这是一段很长很长很长的描述性文字这是一段很长很长很长的描述性文字"></el-step>
      <el-step title="步骤3" description="这是一段很长很长很长的描述性文字这是一段很长很长很长的描述性文字"></el-step>
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
