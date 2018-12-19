<template>
  <div class="home">
    <el-container class="main-container">
    <el-header>
      <custom_header></custom_header>
    </el-header>
    <el-main>
      <search_table_menu></search_table_menu>
    </el-main>
    <el-footer>
      <custom_footer></custom_footer>
    </el-footer>
    </el-container>
    
  </div>
</template>

<script>
// @ is an alias to /src
/* eslint-disable */
import custom_header from '@/components/nav-header.vue'
import search_table_menu from '@/components/search-table-menu.vue'
import custom_footer from '@/components/nav-footer.vue'

export default {
  name: 'home',
  components: {
    custom_header,
    search_table_menu,
    custom_footer
  },
}
</script>

<style scoped>
.el-header {
    padding: 0;
    text-align: center;
    line-height: 60px;
  }
.el-footer {
  margin-bottom: 0;
  padding: 0;
  color:white;
  height: 300px;
  background-color: rgb(84, 92, 100);
  text-align: center;
  /* line-height: 300px; */
}
body > .el-container {
    margin-bottom: 0;
  }
.main-container{
    display: flex;  /* 自适应屏幕高度*/
    min-height: 100vh;  /* 自适应屏幕高度*/
    flex-direction: column;  /* 自适应屏幕高度*/
  }
.el-main {
  padding: 0;
}

</style>

