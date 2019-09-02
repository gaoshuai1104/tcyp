<template>

<el-row class="tac">
  <el-col :span="4">
    <el-menu
    :default-active="$route.path" router
    :collapse-transition=false
    default-openeds=[1,2,4]
      class="el-menu-vertical-demo"
      @open="handleOpen"
      @close="handleClose"
      background-color="#545c64"
      text-color="#fff"
      active-text-color="#ffd04b">
      <el-submenu index="1">
        <template slot="title">
          <i class="el-icon-menu"></i>
          <span>智慧门禁</span>
        </template>
        <div class="child">
      <el-menu-item-group>
      <el-menu-item index="/Admission">进入登记</el-menu-item>
      <el-menu-item index="/Leavingschool">离开登记</el-menu-item>
      <el-menu-item index="/list">访客列表</el-menu-item>
      <el-menu-item index="/information">访客信息</el-menu-item>
      </el-menu-item-group>
      </div>
      </el-submenu>

      <el-submenu index="/Security">
        <template slot="title">
          <i class="el-icon-menu"></i>
          <span>安防监控</span>
        </template>
        <div class="child">
            <!-- <el-menu-item-group>
      <el-menu-item index="/OrderApply" >输入采购订单</el-menu-item>
      <el-menu-item index="/Orderquery" >采购订单列表</el-menu-item>
      </el-menu-item-group> -->
      </div>
      </el-submenu>
      <!-- <el-menu-item disabled index="/Receivinggoods">
        <i class="el-icon-menu"></i>
        <span slot="title">收货管理</span>
      </el-menu-item> -->
      <el-submenu index="/Guidance">
        <template slot="title">
          <i class="el-icon-menu"></i>
          <span>小区导引</span>
        </template>
        <div class="child">
        <el-menu-item-group>
      <el-menu-item index="/warehousingApply" >输入采购入库</el-menu-item>
      <el-menu-item index="/warehousingQuery" >查询采购入库</el-menu-item>
      </el-menu-item-group>
      </div>
      </el-submenu>
      <el-menu-item index="5">
        <i class="el-icon-menu"></i>
        <span slot="title">异情分析</span>
      </el-menu-item>
      <el-menu-item index="6">
        <i class="el-icon-menu"></i>
        <span slot="title">应急模拟</span>
      </el-menu-item>
      <!-- <el-menu-item index="7">
        <i class="el-icon-menu"></i>
        <span slot="title">财务协同管理</span>
      </el-menu-item>
            <el-menu-item index="8">
        <i class="el-icon-menu"></i>
        <span slot="title">供应商管理</span>
      </el-menu-item> -->
    </el-menu>
  </el-col>
</el-row>
</template>
<script>
  export default {
    data() {
      return {
        activeIndex: '1'
      }
    },
    methods: {
      handleOpen(key, keyPath) {
    
      console.log(key, keyPath);
    },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
    }
    }
</script>
<style>
.tac{
  top: 120px;
  left: -20px;
  position: fixed;
  background-color: rgb(84, 92, 100);
  width: 160px;
}
/* .el-submenu__title,.el-menu-item{
  width: 200px;
} */
.el-table td, .el-table th.is-leaf{
  border-bottom: 1px solid rgb(84, 92, 100);
  border-left: 1px solid rgb(84, 92, 100);
}

.el-table{
  border: 1px solid rgb(84, 92, 100); 
}
.tac .el-menu-item-group__title{
      background-color: rgb(84, 92, 100);
}
.child{
  margin-left: 20px;
}
.el-submenu .el-menu-item,.el-submenu__title{
  height: 30px;
  line-height: 30px;
  text-align: left;
}
.el-submenu .el-menu-item{
  min-width: 140px;
}
.el-icon-arrow-down:before{
  display: none;
}
</style>
