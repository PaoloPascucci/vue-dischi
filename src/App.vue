<template>
  <div id="app">
    <SiteHeader/>
    <SiteMain/>
  </div>
</template>

<script>
// import axios from 'axios'
import SiteHeader from './components/SiteHeader.vue'
import SiteMain from './components/SiteMain.vue'
import '../node_modules/bootstrap/scss/bootstrap.scss';

export default {
  name: 'App',
  components: {
    // axios, 
    SiteHeader,
    SiteMain
  }
}
</script>

<style lang="scss">
@import '../node_modules/bootstrap/scss/bootstrap.scss';
// #app {
//   // font-family: Avenir, Helvetica, Arial, sans-serif;
//   // -webkit-font-smoothing: antialiased;
//   // -moz-osx-font-smoothing: grayscale;
//   // text-align: center;
//   // color: #2c3e50;
//   // margin-top: 60px;
// }
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
