<template>
  <div id="app">
    <div class="block">
      <span>默认</span><br>
      <el-date-picker
        v-model="value1"
        type="date"
        placeholder="选择日期"
      ></el-date-picker>
    </div>
    <div class="block">
      <span>带快捷选项</span><br>
      <el-date-picker
        v-model="value2"
        align="right"
        type="date"
        placeholder="选择日期"
        :picker-options="pickerOptions"
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
        pickerOptions: {
          disabledDate(time) {
            return time.getTime() > Date.now() || time.getTime() < Date.now() - 10 * 3600 * 1000 * 24;
          },
          shortcuts: [
            {
              text: "今天",
              onClick(picker) {
                picker.$emit("pick", new Date())
              }
            },
            {
              text: "昨天",
              onClick(picker) {
                const date = new Date()
                date.setTime(date.getTime() - 3600 * 1000 * 24);
                picker.$emit("pick", date)
              }
            },
            {
              text: "一周前",
              onClick(picker) {
                let date = new Date();
                date.setTime(date.getTime() - 3600 * 1000 * 24 * 7)
                picker.$emit("pick", date)
              }
            }
          ]
        },
        value1: "",
        value2: ""
      }
    },
    methods: {}
  };
</script>

<style lang="less">
</style>
