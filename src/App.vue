<template>
  <div id="app">
    <el-time-picker
      v-model="value1"
      picker-options="{
        selectableRange: '18:30:00 - 20:30:00'
      }"
      placeholder="任意时间点"
    ></el-time-picker>
    <el-time-picker
      arrow-control
      v-model="value2"
      :picker-options="{
        selectableRange: '18:30:00 - 20:30:00'
      }"
      placeholder="任意时间点"
    ></el-time-picker>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        value1: new Date(2016, 9, 10, 18, 40),
        value2: new Date(2016, 9, 10, 18, 40),
      }
    },
    methods: {
    }
  };
</script>

<style lang="less">
</style>
