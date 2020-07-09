<template>
  <div id="app">
    <div>
      <el-radio v-model="radio1" label="1" border>备选项</el-radio>
      <el-radio v-model="radio1" label="2" border>备选项</el-radio>
    </div>
    <div style="margin-top: 20px">
      <el-radio v-model="radio2" label="1" border size="medium">备选项</el-radio>
      <el-radio v-model="radio2" label="2" border size="medium">备选项</el-radio>
    </div>
    <div style="margin-top: 20px">
      <el-radio-group v-model="radio3" size="small">
        <el-radio label="1" border>备选项</el-radio>
        <el-radio label="2" border disabled>备选项</el-radio>
      </el-radio-group>
    </div>
    <div style="margin-top: 20px;">
      <el-radio-group v-model="radio4" size="mini" disabled>
        <el-radio label="1" border>备选项</el-radio>
        <el-radio label="2" border>备选项</el-radio>
      </el-radio-group>
    </div>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      radio1: "1",
      radio2: "1",
      radio3: "1",
      radio4: "上海",
    }
  },
  methods: {
    changeFn(val) {
      console.log(val);
    }
  },
};
</script>

<style lang="less">
</style>
