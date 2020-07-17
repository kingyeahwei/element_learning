<template>
  <div id="app">
    <el-dropdown :hide-on-click="false">
      <span class="el-dropdown-link">
        下拉菜单 <i class="el-icon-arrow-down el-icon--right"></i>
      </span>
      <el-dropdown-menu slot="dropdown">
        <el-dropdown-item>黄金糕</el-dropdown-item>
        <el-dropdown-item>黄金糕</el-dropdown-item>
        <el-dropdown-item>黄金糕</el-dropdown-item>
        <el-dropdown-item disabled>黄金糕</el-dropdown-item>
        <el-dropdown-item divided>黄金糕</el-dropdown-item>
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
