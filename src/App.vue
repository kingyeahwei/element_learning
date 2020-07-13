<template>
  <div id="app">
    <el-rate
      v-model="value"
      :icon-classes="iconClasses"
      void-icon-class="icon-rate-face-off"
      :colors="['#99A9BF', '#F7BA2A', '#FF9900']">
    </el-rate>
  </div>
</template>

<script>
  let id = 0;
  export default {
    name: "app",
    data() {
      return {
        value: null,
        iconClasses: ['icon-rate-face-1', 'icon-rate-face-2', 'icon-rate-face-3']
      };
    },
    methods: {}
  };
</script>

<style lang="less">
</style>
