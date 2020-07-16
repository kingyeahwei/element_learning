<template>
  <div id="app">
    <el-table
    :data="filterHandle"
    style="width: 100%">
      <el-table-column label="Date" prop="date"></el-table-column>
      <el-table-column label="Name" prop="name"></el-table-column>
      <el-table-column align="right">
        <template slot-scope="scope" slot="header">
          <el-input v-model="search" size="mini" placeholder="输入关键字搜索"></el-input>
        </template>
        <template slot-scope="scope">
          <el-button size="mini" @click="handleEdit(scope.$index, scope.row)">edit</el-button>
          <el-button size="mini" type="danger" @click="handleDelete(scope.$index, scope.row)">delete</el-button>
        </template>
      </el-table-column>
    </el-table>
  </div>
</template>

<script>
    export default {
        name: "app",
        data() {
            return {
                tableData: [
                    {
                        date: '2016-05-02',
                        name: '王大虎',
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
                ],
                search: ""
            }
        },
        methods: {
            handleEdit(index, row) {
                console.log(index, row);
            },
            handleDelete(index, row) {
                console.log(index, row);
            },
        },
        computed: {
            filterHandle() {
                let _this = this
                return this.tableData.filter((data) => {
                    return  !_this.search || data.name.toLowerCase().includes(_this.search.toLowerCase())
                })
            }
        }
    };
</script>

<style lang="less">
</style>
