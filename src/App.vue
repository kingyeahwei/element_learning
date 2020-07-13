<template>
  <div id="app">
    <div class="block">
      <span>起始日期时刻为 12:00:00</span>
      <el-date-picker
        v-model="value1"
        type="datetimerange"
        start-placeholder="开始日期"
        end-placeholder="结束日期"
        :default-time="['12:00:00']"
      ></el-date-picker>
    </div>
    <div class="block">
      <span>起始日期时刻为 12:00:00 结束日期时刻为 08:00:00</span>
      <el-date-picker
        v-model="value2"
        type="datetimerange"
        align="right"
        start-placeholder="开始日期"
        end-placeholder="结束日期"
        :default-time="['12:00:00', '08:00:00']"
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
        value2: ""
      };
    },
    methods: {}
  };
</script>

<style lang="less">
</style>
