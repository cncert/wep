<template>
  <div>
      <el-menu 
        class="el-menu-demo"
        mode="horizontal"
        @select="handleSelect"
        background-color="#545c64"
        text-color="#fff"
        active-text-color="#ffd04b">
        <el-menu-item index="1">LOGO</el-menu-item>
        <el-menu-item index="2">
            <div class="demo-input-suffix">
                <el-input
                placeholder="请输入搜索内容"
                v-model="search_key" size="small"
                @keyup.enter.native="onSubmit"
                >
                <i slot="prefix" class="el-input__icon el-icon-search"></i>
                </el-input>
            </div>
        </el-menu-item>
        <el-menu-item index="3">
            <i class="el-icon-star-off"></i>成为宠物保姆
        </el-menu-item>
        <el-submenu index="4" >
                <template slot="title"><i class="el-icon-menu"></i>我们的服务</template> 
                <el-menu-item index="4-1">服务1</el-menu-item>
                <el-menu-item index="4-2">服务2</el-menu-item>
                <el-menu-item index="4-3">服务3</el-menu-item>
           
        </el-submenu>
        <div>
            <el-menu-item index="5"  class="align-right">登陆</el-menu-item>
        </div>
        <div>
            <el-menu-item index="6"  class="align-right">注册</el-menu-item>
        </div>
        
      </el-menu>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'nav-header',
  components: {
  },
    data() {
        return {
            search_key:''
            
        };
    },
    methods: {
        handleSelect(key, keyPath) {
            console.log(key, keyPath);
        }
    }
}
</script>

<style scoped>
  /*修改默认的样式：新建一个style，不加scoped*/
 .el-menu--horizontal /deep/ .el-submenu__title{
    font-size: 16px;
  }
  .el-menu--horizontal >.el-menu-item{
      font-size: 16px;
  }
  .align-right{
      float: right;
      font-size: 16px;
  }
</style>