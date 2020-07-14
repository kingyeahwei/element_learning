<template>
  <div id="app">
    <el-transfer
      v-model="value"
      :props="{key: 'value', label: 'desc'}"
      :data="data"
    ></el-transfer>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      const generateData = () => {
        const data = [];
        for (let i = 1; i <= 15; i++) {
          data.push({
            value: i,
            desc: `备选项${i}`,
            disabled: i % 4 === 0
          })
        }
        return data;
      }
      return {
        data: generateData(),
        value: []
      }
    },
    methods: {
    }
  };
</script>

<style lang="less">
</style>
