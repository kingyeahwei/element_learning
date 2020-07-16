<template>
  <div id="app">
    <el-switch v-model="value">
    </el-switch>
    <el-pagination
      :hide-on-single-page="value"
      :total="5"
      layout="prev, pager, next">
    </el-pagination>
  </div>
</template>

<script>
  export default {
    name: "app",
    data() {
      return {
        value: false
      }
    },
    methods: {
    }
  }
</script>

<style lang="less">
</style>
