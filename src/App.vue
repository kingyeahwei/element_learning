<template>
  <div id="app">
    <el-transfer
      v-model="value"
      :data="data"
    ></el-transfer>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      const generateData = (_) => {
        const data = [];
        for (let i = 1; i <= 15; i++) {
          data.push({
            key: i,
            label: `备选项${i}`,
            disable: i % 4 == 0
          })
        }
        return data
      }
      return {
        data: generateData(),
        value: [1, 4]
      };
    },
    methods: {}
  };
</script>

<style lang="less">
</style>
