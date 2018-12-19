<template>
  <div id="app">
      <home>
      </home>
  </div>
</template>

<script>
import home from './views/Home.vue'

export default {
  name: 'app',
  components: {
    home
  }
}
</script>

<style>
body {
  /* 修改body样式 */
  margin-top: 0;
  margin-bottom: 0;
  margin-left: 0;
  margin-right: 0;
  /* background: url('assets/homepage.jpg'); */
  
}
.el-menu.el-menu--horizontal {
  border-bottom: solid 0px !important
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
