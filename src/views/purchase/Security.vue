<template>
<div class="af">
<el-container>
  <el-aside width="200px">
        <el-col :span="24">
         <el-menu
      default-active="2"
      class="el-menu-vertical-demo"
      @open="handleOpen"
      @close="handleClose">
      <el-submenu index="1">
        <template slot="title">
          <i class="el-icon-location"></i>
          <span>A栋区域</span>
        </template>
        <el-menu-item-group>
          <el-menu-item index="1-1">A-1</el-menu-item>
          <el-menu-item index="1-2">A-2</el-menu-item>
          <el-menu-item index="1-1">A-3</el-menu-item>
          <el-menu-item index="1-2">A-4</el-menu-item>
        </el-menu-item-group>
      </el-submenu>
            <el-submenu index="2">
        <template slot="title">
          <i class="el-icon-location"></i>
          <span>B栋区域</span>
        </template>
        <el-menu-item-group>
          <el-menu-item index="2-1">B-1</el-menu-item>
          <el-menu-item index="2-2">B-2</el-menu-item>
          <el-menu-item index="2-1">B-3</el-menu-item>
          <el-menu-item index="2-2">B-4</el-menu-item>
        </el-menu-item-group>
      </el-submenu>
            <el-submenu index="3">
        <template slot="title">
          <i class="el-icon-location"></i>
          <span>C栋区域</span>
        </template>
        <el-menu-item-group>
          <el-menu-item index="3-1">C-1</el-menu-item>
          <el-menu-item index="3-2">C-2</el-menu-item>
          <el-menu-item index="3-1">C-3</el-menu-item>
          <el-menu-item index="3-2">C-4</el-menu-item>
        </el-menu-item-group>
      </el-submenu>
            <el-submenu index="4">
        <template slot="title">
          <i class="el-icon-location"></i>
          <span>D栋区域</span>
        </template>
        <el-menu-item-group>
          <el-menu-item index="4-1">D-1</el-menu-item>
          <el-menu-item index="4-2">D-2</el-menu-item>
          <el-menu-item index="4-1">D-3</el-menu-item>
          <el-menu-item index="4-2">D-4</el-menu-item>
        </el-menu-item-group>
      </el-submenu>
     
    </el-menu>
  </el-col>
  </el-aside>
  <el-container>
    <el-header>汤臣一品接警中心</el-header>
    <el-main id="lh">视频区</el-main>
    <el-footer>报警原因： 检测到越界人员，请通知安保人员及时排查</el-footer>
  </el-container>
</el-container>
</div>
</template>
<script>
export default {
    
}
</script>
<style lang="less" scoped>
    .bg{
        font-size: 50px;
    }
    .af{
      margin-top: 50px;
    }
</style>
<style>
  .el-header, .el-footer {
    background-color: #B3C0D1;
    color: #333;
    text-align: center;
    line-height: 60px;
  }
  
  .el-aside {
    background-color: #D3DCE6;
    color: #333;
    text-align: center;
    /* line-height: 200px; */
  }
  
#lh {
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
    line-height: 300px;
    height: 100%;
  }
  
  body > .el-container {
    margin-top: 100px;
    line-height: 50px;
  }
</style>