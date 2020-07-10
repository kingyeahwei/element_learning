<template>
  <div id="app">
    <div class="demo-input-size">
      <el-input v-model="input1" placeholder="请输入内容" suffix-icon="el-icon-date"></el-input>
      <el-input v-model="input2" placeholder="请输入内容" size="medium" suffix-icon="el-icon-date"></el-input>
      <el-input v-model="input3" suffix-icon="el-icon-date" size="small" placeholder="请输入内容"></el-input>
      <el-input v-model="input4" placeholder="请输入内容" suffix-icon="el-icon-date" size="mini"></el-input>
    </div>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      input1: "",
      input2: "",
      input3: "",
      input4: ""
    };
  },
  methods: {}
};
</script>

<style lang="less">
</style>
