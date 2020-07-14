<template xmlns="http://www.w3.org/1999/html">
  <div id="app">
    <el-form :model="formInline" class="demo-form-inline" :inline="true">
      <el-form-item label="审批人">
        <el-input v-model="formInline.user" placeholder="审批人"></el-input>
      </el-form-item>
      <el-form-item label="活动区域">
        <el-select v-model="formInline.region" placeholder="活动区域">
          <el-option label="区域1" value="shanghai"></el-option>
          <el-option label="区域2" value="beijing"></el-option>
        </el-select>
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="onSubmit">查询</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        formInline: {
          user: "",
          region: ""
        }
      }
    },
    methods: {
      onSubmit() {
        console.log("submit!!")
      }
    }
  };
</script>

<style lang="less">
</style>
