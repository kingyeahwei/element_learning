<template>
  <div id="app">
    <div class="demo-image-error">
      <div class="block">
        <span>默认</span>
        <el-image></el-image>
      </div>
      <div class="block">
        <span>自定义</span>
        <el-image>
          <div slot="error" class="image-slot">
            <i class="el-icon-picture-outline"></i>
          </div>
        </el-image>
      </div>
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
  .is-selected {
    color: #1989fa;
  }
</style>
