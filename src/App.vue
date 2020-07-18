<template>
  <div id="app">
    <el-button type="text" @click="table = true">打开嵌套表格的Drawer</el-button>
    <el-button type="text" @click="dialog = true">打开嵌套Form的Drawer</el-button>

    <el-drawer
      title="我嵌套了表格"
      :visible.sync="table"
      direction="rtl"
      size="50%">
      <el-table :data="girdData">
        <el-table-column property="date" label="日期" width="150"></el-table-column>
        <el-table-column property="name" label="姓名" width="200"></el-table-column>
        <el-table-column property="address" label="地址"></el-table-column>
      </el-table>
    </el-drawer>
    <el-drawer
      title="我嵌套了form"
      :before-close="handleClose"
      :visible.sync="dialog"
      direction="ltr"
      custom-class="demo-drawer"
      ref="drawer">
      <div class="demo-drawer__content">
        <el-form :model="form">
          <el-form-item
            label="活动名称"
            :label-width="formLabelWidth">
            <el-input v-model="form.name" autocomplete="off"></el-input>
          </el-form-item>
          <el-form-item label="活动区域" :label-width="formLabelWidth">
            <el-select v-model="form.region" placeholder="请选择活动区域">
              <el-option label="区域一" value="shanghai"></el-option>
              <el-option label="区域二" value="beijing"></el-option>
            </el-select>
          </el-form-item>
          <div class="demo-drawer__footer">
            <el-button @click="cancelForm">取消</el-button>
            <el-button type="primary" @click="$refs.drawer.closeDrawer()" :loading="loading">{{loading ? "提交中" :
              "确定"}}
            </el-button>
          </div>
        </el-form>
      </div>
    </el-drawer>
  </div>
</template>

<script>
  export default {
    name: "app",
    data() {
      return {
        table: false,
        dialog: false,
        loading: false,
        girdData: [
          {
            date: '2016-05-02',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1518 弄'
          }, {
            date: '2016-05-04',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1518 弄'
          }, {
            date: '2016-05-01',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1518 弄'
          }, {
            date: '2016-05-03',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1518 弄'
          }
        ],
        form: {
          name: "",
          region: "",
          date1: "",
          date2: "",
          delivery: "",
          type: [],
          resource: "",
          desc: ""
        },
        formLabelWidth: "80px",
        timer: null,
      }
    },
    methods: {
      handleClose(done) {
        if (this.loading) {
          return;
        }
        this.$confirm("确定要提交表单吗?")
          .then(() => {
            this.loading = true;
            this.timer = setTimeout(() => {
              done();
              setTimeout(() => {
                this.loading = false
              }, 400)
            }, 2000)
          })
          .catch(() => {
          })

      },
      cancelForm() {
        this.loading = false;
        this.dialog = false;
        clearTimeout(this.timer)
      }
    }
  }
</script>

<style lang="less">
</style>
