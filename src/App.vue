<template>
  <div id="app">
    <el-transfer
      filterable
      :filter-method="filterMethod"
      filter-placeholder="请输入城市拼音"
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
        const cities = ["上海", "北京", "广州", "深圳", "南京", "西安", "成都"];
        const pinyin = ["shanghai", "beijing", 'guangzhou', "shenzhen", 'nanjing', 'xian', 'chengdu'];
        cities.forEach((item, index) => {
          data.push({
            label: item,
            key: index,
            pinyin: pinyin[index]
          });
        });
        return data;
      };
      return {
        data: generateData(),
        value: [],
      }
    },
    methods: {
      filterMethod(query, item) {
        console.log(query)
        console.log(item)
        return item.pinyin.indexOf(query) > -1;
      }
    }
  };
</script>

<style lang="less">
</style>
