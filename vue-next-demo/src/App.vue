<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  components: {}
})
export default class App extends Vue {}
</script>

<style lang="less">
@import url('../src/css/common.less');
* {
  padding: 0;
  margin: 0;
  font-family: 'Open Sans Light';
  letter-spacing: 0.05em;
}
html {
  height: 100%;
}
body {
  min-width: 320px;
  width: 15rem;
  height: 100%;
  margin: 0 auto !important;
  line-height: 1.5;
  font-family: Arial, Helvetica;
}
#app {
  height: 100%;
}
</style>
