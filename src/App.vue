<template>
  <div id="app">
    <el-cascader :props="props"></el-cascader>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        props: {
          lazy: true,
          lazyLoad(node, resolve) {
            const {level} = node;
            setTimeout(() => {
              const nodes =  Array.from({length: level + 1}).map((item) => {
                return {
                  value: ++id,
                  label: `选项${id}`,
                  leaf: level >= 2
                }
              })
              resolve(nodes);
            }, 1000)
          }
        }
      }
    }
  };
</script>

<style lang="less">
</style>
