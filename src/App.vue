<template>
  <div id="app">
    <div class="block">
      <span>周</span><br>
      <el-date-picker
        v-model="value1"
        type="week"
        format="yyyy 年 WW 周"
        placeholder="选择周"
      ></el-date-picker>
    </div>
    <div class="block">
      <span>月</span><br>
      <el-date-picker
        v-model="value2"
        type="month"
        placeholder="选择月"
      ></el-date-picker>
    </div>
    <div class="block">
      <span>年</span><br>
      <el-date-picker
        v-model="value3"
        type="year"
        placeholder="选择年"
      ></el-date-picker>
    </div>
    <div class="block">
      <span>多个日期</span><br>
      <el-date-picker
        type="dates"
        v-model="value4"
        placeholder="选择一个或者多个日期"
      ></el-date-picker>
    </div>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        value1: "",
        value2: "",
        value3: "",
        value4: []
      }
    },
    methods: {}
  };
</script>

<style lang="less">
</style>
