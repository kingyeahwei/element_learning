<template>
  <div id="app">
    <div class="block">
      <span>默认为Date对象</span>
      <div>值: {{value1}}</div>
      <el-date-picker
        v-model="value1"
        type="date"
        placeholder="选址日期"
        format="yyyy 年 MM 月 dd 日"
      ></el-date-picker>
    </div>
    <div class="block">
      <span>使用value-format</span>
      <div>值: {{value2}}</div>
      <el-date-picker
        v-model="value2"
        type="date"
        placeholder="选择日期"
        format="yyyy 年 MM 月 dd 日"
        value-format="yyyy-MM-dd"
      ></el-date-picker>
    </div>
    <div class="block">
      <span>时间戳</span>
      <div>值: {{value3}}</div>
      <el-date-picker
        v-model="value3"
        type="date"
        placeholder="选择日期"
        format="yyyy 年 MM 月 dd 日"
        value-format="timestamp"
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
        value3: ""
      };
    },
    methods: {}
  };
</script>

<style lang="less">
</style>
