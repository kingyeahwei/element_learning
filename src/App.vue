<template>
  <div id="app">
    <el-select v-model="value" placeholder="请选择">
      <el-option-group v-for="group in options" :key="group.label" :label="group.label">
        <el-option v-for="item in group.options" :key="item.value" :label="item.label" :value="item.value"></el-option>
      </el-option-group>
    </el-select>
  </div>
</template>

<script>
  export default {
    name: "app",
    data() {
      return {};
    },
    methods: {}
  };
</script>

<style lang="less">
</style>
