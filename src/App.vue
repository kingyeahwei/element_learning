<template>
  <div id="app">
    <el-input v-model="filterText" placeholder="输入关键字过滤"></el-input>
    <el-tree
      class="filter-tree"
      :data="data"
      :props="defaultProps"
      default-expand-all
      :filter-node-method="filterNode"
      ref="tree"
    ></el-tree>

  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        filterText: "",
        data: [
          {
            id: 1,
            label: '一级 1',
            children: [{
              id: 4,
              label: '二级 1-1',
              children: [{
                id: 9,
                label: '三级 1-1-1'
              }, {
                id: 10,
                label: '三级 1-1-2'
              }]
            }]
          }, {
            id: 2,
            label: '一级 2',
            children: [{
              id: 5,
              label: '二级 2-1'
            }, {
              id: 6,
              label: '二级 2-2'
            }]
          }, {
            id: 3,
            label: '一级 3',
            children: [{
              id: 7,
              label: '二级 3-1'
            }, {
              id: 8,
              label: '二级 3-2'
            }]
          }
        ],
        defaultProps: {
          children: "children",
          label: "label"
        }
      }
    },
    methods: {
      filterNode(value, data) {
        console.log(value);
        console.log(data);
        if (!value) {
          return true;
        }
        return data.label.indexOf(value) !== -1;
      }
    },
    watch: {
      filterText(val) {
        this.$refs.tree.filter(val)
      }
    }
  };
</script>

<style lang="less">
</style>
