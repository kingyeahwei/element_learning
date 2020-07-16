<template>
  <div id="app">
    <el-badge value="12" class="item">
      <el-button size="small">评论</el-button>
    </el-badge>
    <el-badge value="3" class="item">
      <el-button size="small">回复</el-button>
    </el-badge>
    <el-badge value="1" class="item" type="primary">
      <el-button size="small">评论</el-button>
    </el-badge>
    <el-badge value="2" class="item" type="warning">
      <el-button size="small">回复</el-button>
    </el-badge>
    <el-dropdown trigger="click">
      <span class="el-dropdown-link">
        点我查看<i class="el-icon-caret-bottom el-icon-right"></i>
      </span>
      <el-dropdown-menu slot="dropdown">
        <el-dropdown-item>
          <el-badge value="12">
            <el-button type="text">评论</el-button>
          </el-badge>
        </el-dropdown-item>
        <el-dropdown-item>
          回复
          <el-badge value="3"></el-badge>
        </el-dropdown-item>
      </el-dropdown-menu>
    </el-dropdown>
  </div>
</template>

<script>
  export default {
    name: "app",
    data() {
      return {}
    },
    methods: {}
  }
</script>

<style lang="less">
  .item {
    margin-top: 10px;
    margin-right: 40px;
  }
</style>
