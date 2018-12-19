<template>
<div>
    <el-form style="text-align:left" :inline="true" :model="formInline" class="demo-form-inline" label-position='top'>
        <div>
            <el-col :span="12">
                <el-form-item label="寄宿地址" style="width: 100%;" >
                    <el-input v-model="formInline.user" placeholder="寄宿地址"></el-input>
                </el-form-item>
            </el-col>
            <el-col class="line" :span="1">&nbsp;&nbsp;</el-col>
            <el-col :span="11">
                <el-form-item label="开始与结束日期" style="width: 100%;">
                    <el-date-picker  style="width: 100%;"
                        v-model="value6"
                        type="daterange"
                        range-separator="至"
                        start-placeholder="开始日期"
                        end-placeholder="结束日期">
                    </el-date-picker>
                </el-form-item>
            </el-col>
        </div>
        <div>
            <el-col :span="18">
                <el-form-item label="宠物体型" style="width: 100%;" >
                    <el-checkbox-group v-model="pet_size">
                        <el-checkbox-button type="primary" v-for="size in pet_size_set" :label="size.weight" :key="size.id">
                            <div>{{size.size}}</div>
                            <div>{{size.weight}}kg</div>
                            
                            </el-checkbox-button>
                    </el-checkbox-group>
                </el-form-item>
            </el-col>
            <el-col :span="6">
                <el-form-item label="." style="width: 100%;" >
                    <el-button  class="button-font"  type="success">查  找</el-button>
                </el-form-item> 
            </el-col>
        </div>
    </el-form>
</div>
</template>

<script>
export default {
    name: 'search-table',
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
            sizeForm: {
            name: '',
            region: '',
            date1: '',
            date2: '',
            delivery: false,
            type: [],
            resource: '',
            desc: ''
            },
            pet_size: [],
            pet_size_set: [
                {'size': '小型', 'weight': '0-15'},
                {'size': '中型', 'weight': '16-50'},
                {'size': '大型', 'weight': '50+'},
            ],
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
      width: 150px;
      height: 60px;
      margin-right: 15px;
      border: 1px solid #dcdfe6;
      border-radius: 4px !important
  }
  .custom-search {
      padding-bottom: 300px;
  }
</style>

