<template>
  <div id="app">
    <el-time-select
      placeholder="起始时间"
      v-model="startTime"
      :picker-options="{
        start: '08:30',
        step: '00:15',
        end: '18:30',
        maxTime: endTime
      }"
    ></el-time-select>
    <el-time-select
      placeholder="结束时间"
      v-model="endTime"
      :picker-options="{
        start: '08:30',
        step: '00:15',
        end: '18:30',
        minTime: startTime
      }"
    ></el-time-select>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        startTime: "",
        endTime: ""
      }
    },
    methods: {
    }
  };
</script>

<style lang="less">
</style>
