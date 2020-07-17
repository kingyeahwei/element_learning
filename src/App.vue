<template>
  <div id="app">
    <el-card>
      <div v-for="o in 4" :key="o" class="text item">
        {{"列表内容" + o}}
      </div>
    </el-card>
  </div>
</template>

<script>
    export default {
        name: "app",
        data() {
            return {
            }
        },
        methods: {
        }
    }
</script>

<style lang="less">
  .text {
    font-size: 14px;
  }
  .item {
    margin-bottom: 18px;
  }
  .box-card {
    width: 480px;
  }
</style>
