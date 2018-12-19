<template>
    <div class="note" :style ="note">
        <div style="font-size: 50px; color:white;">
            <span class="home-page-text">关心我们的爱宠</span>
        </div>
        <div class="custom-search">
            <el-row>
                <el-col :span="4"><div class="grid-content bg-purple"></div></el-col>
                <el-col :span="16">
                    <div class="grid-content bg-purple-light">
                        <div class="select-pet-name" center="true">
                            为您的宠物寻找服务: &nbsp;&nbsp;
                            <el-radio-group v-model="check_radio">
                                <el-radio :label="1">狗狗</el-radio>
                                <el-radio :label="2">猫咪</el-radio>
                            </el-radio-group>
                        </div>
                        <el-tabs type="border-card" >
                            <el-tab-pane>
                                <span slot="label">宠物寄宿</span>
                                <search_table></search_table>
                            </el-tab-pane>
                            <el-tab-pane>
                                <span slot="label">宠物寄养</span>
                                <search_table></search_table>
                            </el-tab-pane>
                            <el-tab-pane>
                                <span slot="label">宠物串门</span>
                                <search_table></search_table>
                            </el-tab-pane>
                            <el-tab-pane>
                                <span slot="label">宠物日托</span>
                                <search_table></search_table>
                            </el-tab-pane>
                            <el-tab-pane>
                                <span slot="label">宠物散步</span>
                                <search_table></search_table>
                            </el-tab-pane>
                            
                        </el-tabs>
                    </div>
                </el-col>
                <el-col :span="4"><div class="grid-content bg-purple"></div></el-col>
            </el-row>
        </div>
    </div>
    
</template>

<script>
import search_table from '@/components/search-table.vue'
export default {
    name: 'search-table-menu',
    components: {
        search_table,
    },
    data() {
        return {
            value6: '',
            check_radio: 1,
            note: {
                backgroundImage: "url(" + require("../assets/new.jpg") + ")",
                backgroundRepeat: "no-repeat",
                backgroundSize: "cover",
                backgroundPosition:"center",
                backgroundAttachment:"fixed",
                marginTop: "0",
            },
            formInline: {
                user: '',
                region: ''
            },
        }
    
    }
}
</script>


<style scoped>
.home-page-text {
    margin-top:10%;
    display:inline-block;
    margin-bottom: 5%
}
.select-pet-name {
    height:50px; 
    line-height: 50px;
    text-align: left;
    margin-left: 20px
}
.button-font {
    width: 100%;
    height: 60px;
}

.el-row {
    margin-bottom: 20px;
    
  }
  .el-col {
    border-radius: 4px;
  }
  .bg-purple-dark {
    background: #99a9bf;
  }
  
  .bg-purple-light {
    background: #e5e9f2;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
  .el-checkbox-group /deep/ .el-checkbox-button__inner{
      width: 200px;
      height: 60px;
      margin-right: 15px;
      border: 1px solid #dcdfe6;
      border-radius: 4px !important
  }
  .custom-search {
      padding-bottom: 300px;
  }
</style>

