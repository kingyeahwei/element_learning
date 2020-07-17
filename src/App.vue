<template>
  <div id="app">
    <el-calendar>
      <template slot="dateCell" slot-scope="{date, data}">
        <p :class="data.isSelected ? 'is-selected' : ''">
          {{data.day.split("-").slice(1).join("-")}} {{data.isSelected ? "✔" : ""}}
        </p>
      </template>
    </el-calendar>
  </div>
</template>

<script>
  export default {
    name: "app",
    data() {
      return {
        value: new Date(new Date().getTime() - 3600 * 1000 * 24 * 24)
      }
    },
    methods: {
    }
  }
</script>

<style lang="less">
  .is-selected {
    color: #1989fa;
  }
</style>
