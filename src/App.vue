<template>
  <div id="app">
    <el-dropdown @command="handleCommand">
      <span class="el-dropdown-link">
        下拉菜单 <i class="el-icon-arrow-down el-icon--right"></i>
      </span>
      <el-dropdown-menu slot="dropdown">
        <el-dropdown-item command="a">华金糕</el-dropdown-item>
        <el-dropdown-item command="b">狮子头</el-dropdown-item>
        <el-dropdown-item command="c">螺蛳粉</el-dropdown-item>
        <el-dropdown-item command="d">蒜片</el-dropdown-item>
        <el-dropdown-item command="e">蚵仔煎</el-dropdown-item>
      </el-dropdown-menu>
    </el-dropdown>
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
            handleCommand(command) {
                console.log(command)
                this.$message("click on item" + command);
            }
        }
    }
</script>

<style lang="less">
  .el-dropdown-link {
    cursor: pointer;
    color: blue;
  }
  .el-icon-arrow-down {
    color: blue;
  }
</style>
