<template>
  <div id="app">
    <el-time-select
      v-model="value"
      :picker-options="{
        start: '08:30',
        step: '00:15',
        end: '18:30'
      }"
      placeholder="选择时间"
    ></el-time-select>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        value: ""
      }
    },
    methods: {
    }
  };
</script>

<style lang="less">
</style>
