<template>
  <div id="app">
    <span>页数比较少时的效果</span>
    <el-pagination
      layout="prev, pager, next"
      :total="50"
    ></el-pagination>
    <p>大于7页时的效果</p>
    <el-pagination
      layout="prev, pager, next"
      :total="1000"
    ></el-pagination>
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
