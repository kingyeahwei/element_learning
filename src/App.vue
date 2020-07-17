<template>
  <div id="app" style="padding: 300px">
    <el-tooltip content="top center" placement="top">
      <el-button>dark</el-button>
    </el-tooltip>
    <el-tooltip content="bottom center" placement="bottom" effect="light">
      <el-button>light</el-button>
    </el-tooltip>
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
