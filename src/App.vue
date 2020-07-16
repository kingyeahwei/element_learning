<template>
  <div id="app">
    <div class="demo-fit">
      <div class="block" v-for="fit in fits" :key="fit">
        <span class="title">{{fit}}</span>
        <el-avatar shape="square" :size="100" :fit="fit" :src="url"></el-avatar>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "app",
    data() {
      return {
        fits: ['fill', 'contain', 'cover', 'none', 'scale-down'],
        url: 'https://fuss10.elemecdn.com/e/5d/4a731a90594a4af544c0c25941171jpeg.jpeg'
      }
    },
    methods: {
      errorHandler() {
        return true
      }
    }
  }
</script>

<style lang="less">
  .item {
    margin-top: 10px;
    margin-right: 40px;
  }
</style>
