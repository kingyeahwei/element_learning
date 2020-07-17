<template>
  <div id="app">
    <div class="box" style="margin-top: 100px">
      <!--<div class="top">
        <el-tooltip class="item" effect="dark" content="top left 提示文字" placement="top-start">
          <el-button>上左</el-button>
        </el-tooltip>
        <el-tooltip class="item" effect="dark" content="top center 提示文字" placement="top">
          <el-button>上边</el-button>
        </el-tooltip>
        <el-tooltip class="item" effect="dark" content="top right 提示文字" placement="top-end">
          <el-button>上右</el-button>
        </el-tooltip>
      </div>-->

      <!--<div class="left">
        <el-tooltip class="item" effect="dark" content="Left Top 提示文字" placement="left-start">
          <el-button>左上</el-button>
        </el-tooltip>
        <el-tooltip class="item" effect="dark" content="left center 提示文字" placement="left">
          <el-button>左边</el-button>
        </el-tooltip>
        <el-tooltip class="item" effect="dark" content="left bottom 提示文字" placement="left-end">
          <el-button>左下</el-button>
        </el-tooltip>
      </div>-->

      <!--<div class="right">
        <el-tooltip class="item" effect="dark" content="right top 提示文字" placement="right-start">
          <el-button>右上</el-button>
        </el-tooltip>
        <el-tooltip class="item" effect="dark" content="right center 提示文字" placement="right">
          <el-button>右边</el-button>
        </el-tooltip>
        <el-tooltip class="item" effect="dark" content="right bottom 提示文字" placement="right-end">
          <el-button>右下</el-button>
        </el-tooltip>
      </div>-->

      <div class="bottom">
        <el-tooltip class="item" effect="dark" content="bottom left 提示文字" placement="bottom-start">
          <el-button>下左</el-button>
        </el-tooltip>
        <el-tooltip class="item" effect="dark" content="bottom center 提示文字" placement="bottom">
          <el-button>下边</el-button>
        </el-tooltip>
        <el-tooltip class="item" effect="dark" content="bottom right 提示文字" placement="bottom-end">
          <el-button>下右边</el-button>
        </el-tooltip>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "app",
        data() {
            return {
                centerDialogVisible: false
            }
        },
        methods: {
        }
    }
</script>

<style lang="less">
  .box {
    width: 400px;
    margin: auto;

  }
</style>
