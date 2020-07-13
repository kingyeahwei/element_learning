<template>
  <div id="app">
    <div class="block">
      <p>组件值: {{value}}</p>
      <el-date-picker
        v-model="value"
        type="daterange"
        start-placeholder="开始日期"
        end-placeholder="结束日期"
        :default-time="['00:00:00', '23:59:59']"
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
        value: ""
      };
    },
    methods: {}
  };
</script>

<style lang="less">
</style>
