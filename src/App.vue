<template>
  <el-table
    :data="tableData6"
    :span-method="objectSpanMethod"
    border
    style="width: 100%; margin-top: 20px"
  >
    <el-table-column prop="id" label="ID" width="180"></el-table-column>
    <el-table-column prop="name" label="姓名"></el-table-column>
    <el-table-column prop="amount1" label="数值 1（元）"></el-table-column>
    <el-table-column prop="amount2" label="数值 2（元）"></el-table-column>
    <el-table-column prop="amount3" label="数值 3（元）"></el-table-column>
  </el-table>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      spanArr: [],
      tableData6: [
        {
          id: "1",
          name: "王小虎",
          amount1: "234",
          amount2: "3.2",
          amount3: 10,
        },
        {
          id: "1",
          name: "王小虎",
          amount1: "165",
          amount2: "4.43",
          amount3: 12,
        },
        {
          id: "2",
          name: "王小虎",
          amount1: "324",
          amount2: "1.9",
          amount3: 9,
        },
        {
          id: "2",
          name: "王小虎",
          amount1: "621",
          amount2: "2.2",
          amount3: 17,
        },
        {
          id: "2",
          name: "王小虎",
          amount1: "539",
          amount2: "4.1",
          amount3: 15,
        },
      ],
    };
  },
  mounted() {
    this.getSpanArr(this.tableData6);
  },
  methods: {
    getSpanArr(data) {
      for (var i = 0; i < data.length; i++) {
        if (i === 0) {
          this.spanArr.push(1);
          this.pos = 0;
        } else {
          // 判断当前元素与上一个元素是否相同
          if (data[i].id === data[i - 1].id) {
            this.spanArr[this.pos] += 1;
            this.spanArr.push(0);
          } else {
            this.spanArr.push(1);
            this.pos = i;
          }
        }
        console.log(this.spanArr);
      }
    },

    // eslint-disable-next-line no-unused-vars
    objectSpanMethod({ row, column, rowIndex, columnIndex }) {
      if (columnIndex === 0 || columnIndex === 1 || columnIndex === 2) {
        const _row = this.spanArr[rowIndex];
        const _col = _row > 0 ? 1 : 0;
        console.log(`rowspan:${_row} colspan:${_col}`);
        return {
          rowspan: _row, // [0,0] 表示这一行不显示， [2,1]表示行的合并数
          colspan: _col,
        };
      }
    },
  },
};
</script>

<style lang="less">
</style>
