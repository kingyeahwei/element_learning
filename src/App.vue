<template>
  <div id="app">
    <el-table
      :data="tableData"
      :row-class-name="tableRowClassName"
      style="width: 100%">
      <el-table-column
        prop="date"
        label="日期"
        width="180"
      ></el-table-column>
      <el-table-column
        prop="name"
        label="姓名"
        width="180"
      ></el-table-column>
      <el-table-column
        prop="address"
        label="地址"
      ></el-table-column>
    </el-table>
  </div>
</template>

<script>
    let id = 0;
    export default {
        name: "app",
        data() {
            return {
                tableData: [
                    {
                        date: '2016-05-02',
                        name: '王小虎',
                        address: '上海市普陀区金沙江路 1518 弄'
                    }, {
                        date: '2016-05-04',
                        name: '王小虎',
                        address: '上海市普陀区金沙江路 1517 弄'
                    }, {
                        date: '2016-05-01',
                        name: '王小虎',
                        address: '上海市普陀区金沙江路 1519 弄'
                    }, {
                        date: '2016-05-03',
                        name: '王小虎',
                        address: '上海市普陀区金沙江路 1516 弄'
                    }
                ]
            }
        },
        methods: {
            tableRowClassName({row, rowIndex}) {
                if (rowIndex == 1) {
                    return 'warning-row'
                } else if (rowIndex == 3) {
                    return 'success-row'
                }
                return '';
            }
        }
    };
</script>

<style lang="less">
  .el-table .warning-row {
    background: oldlace;
  }
  .el-table .success-row {
    background: #f0f9eb;
  }
</style>
