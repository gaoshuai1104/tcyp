<template>

<el-row class="tac">
  <el-col :span="4" width="100px">
    <el-menu
    :default-active="$route.path" router
    :collapse-transition=false
    default-openeds=[1]
      class="el-menu-demo"
      @open="handleOpen"
      @close="handleClose"
      background-color="#545c64"
      text-color="#fff"
      active-text-color="#ffd04b">
      <el-submenu index="1">
        <template slot="title">
          <i class="el-icon-menu"></i>
          智慧门禁
        </template>
      <el-menu-item index="/Admission">访客登记</el-menu-item>
      <!-- <el-menu-item index="/Leavingschool">离园登记</el-menu-item> -->
      <el-menu-item index="/list">访客列表</el-menu-item>
      <el-menu-item index="/information">访客信息</el-menu-item>
      </el-submenu>
      <el-menu-item index="/Security">
        <template slot="title">
          <i class="el-icon-menu"></i>
          安防监控
        </template>
      </el-menu-item>
      <el-menu-item index="/analyze">
        <i class="el-icon-menu"></i>
        <span slot="title">异情分析</span>
      </el-menu-item>
      <el-menu-item index="Guidance">
        <i class="el-icon-menu"></i>
        <span slot="title">小区导引</span>
      </el-menu-item>
      <el-menu-item index="">
        <i class="el-icon-menu"></i>
        <span slot="title">应急模拟</span>
      </el-menu-item>
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
  left: -23px;
  position: fixed;
  background-color: rgb(84, 92, 100);
  height: 100%;
  width: 140px;
}
.el-table td, .el-table th.is-leaf{
  border-bottom: 1px solid rgb(84, 92, 100);
  border-left: 1px solid rgb(84, 92, 100);
}

.el-table{
  border: 1px solid rgb(84, 92, 100); 
}
.el-submenu .el-menu-item{
  padding: 0;
  min-width: 140px;
}
.el-icon-arrow-down:before{
display: none;
}
.el-menu-item{
  width: 140px;
}
.el-submenu.is-active .el-submenu__title{
  width: 140px;
}
</style>
