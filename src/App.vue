<template>
  <div id="app">
    <ul class="infinite-list" v-infinite-scroll="load" style="overflow:auto">
      <li v-for="i in count" class="infinite-list-item">{{ i }}</li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: "app",
    data() {
      return {
        count: 0
      }
    },
    methods: {
      load () {
        console.log(111)
        this.count += 2
      }
    }
  }
</script>

<style lang="less">
  .infinite-list {
    height: 300px;
    padding: 0;
    margin: 0;
    list-style: none;
  }
  .infinite-list .infinite-list-item {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 50px;
    background: #e8f3fe;
    margin: 10px;
    color: #7dbcfc;
  }
</style>
