<template>
<div>
  <div id="logo">
    <img class="pty" src="../../../static/pty.jpg" alt="">
     <h3>汤臣一品欢迎您!</h3>
  </div>
  <el-menu
    id="bg-top"
    :default-active="activeIndex2"
    class="el-menu-demo"
    mode="horizontal"
    @select="handleSelect"
    background-color="rgb(84, 92, 100)"
    text-color="#fff"
    active-text-color="#ffd04b"
  >
      <el-submenu index="1">
    <template slot="title"><i class="el-icon-s-cooperation" @click="$router.push({ path:'Apply'})"></i>平安住区</template>
    <el-menu-item index="1-1">智慧门禁</el-menu-item>
    <el-menu-item index="1-2">安防监控</el-menu-item>
    <el-menu-item index="1-3">小区导引</el-menu-item>
    <el-menu-item index="1-4">异情分析</el-menu-item>
    <el-menu-item index="1-5">应急模拟</el-menu-item>
    </el-submenu>
      <el-submenu index="2">
    <template slot="title"><i class="el-icon-s-cooperation" @click="$router.push({ path:'Admission'})"></i>贵宾支持</template>
    <el-menu-item index="2-1">到达提醒</el-menu-item>
    <el-menu-item index="2-2">主动服务</el-menu-item>
    </el-submenu>
    
          <el-submenu index="3">
    <template slot="title"><i class="el-icon-s-cooperation"></i>绿色住区</template>
    <el-menu-item index="3-1">垃圾管理</el-menu-item>
    <el-menu-item index="3-2">绿植管理</el-menu-item>
    </el-submenu>
    <el-submenu index="4">
    <template slot="title"><i class="el-icon-s-cooperation"></i>资产管理</template>
    <el-menu-item index="4-1">物业资产台账</el-menu-item>
    <el-menu-item index="4-2">资产卡片</el-menu-item>
    <el-menu-item index="4-3">资产空间分布</el-menu-item>
    <el-menu-item index="4-4">资产查询盘点</el-menu-item>
    <el-menu-item index="4-5">资产关联影响</el-menu-item>
    <el-menu-item index="4-6">资产预算管理</el-menu-item>
    <el-menu-item index="4-7">资产成本分析</el-menu-item>
    </el-submenu>
    <el-submenu index="5">
    <template slot="title"><i class="el-icon-s-cooperation"></i>设备运维</template>
    <el-menu-item index="5-1">设备状态指标</el-menu-item>
    <el-menu-item index="5-2">故障维修</el-menu-item>
    <el-menu-item index="5-3">计划性维护</el-menu-item>
    <el-menu-item index="5-4">预防性维护</el-menu-item>
    <el-menu-item index="5-5">设备维护电子档案</el-menu-item>
    <el-menu-item index="5-6">运维费用统计</el-menu-item>
    </el-submenu>
    <el-submenu index="6">
    <template slot="title"><i class="el-icon-s-cooperation"></i>空间管理</template>
    <el-menu-item index="6-1">空间创收</el-menu-item>
    <el-menu-item index="6-2">空间清册</el-menu-item>
    <el-menu-item index="6-3">空间查询</el-menu-item>
    <el-menu-item index="6-4">空间占用</el-menu-item>
    <el-menu-item index="6-4">费用分摊</el-menu-item>
    </el-submenu>
  </el-menu>
  </div>
</template>
<script>
import dayjs from 'dayjs'
export default {
  data() {
    return {
      dayjs,
      activeIndex: "1",
      activeIndex2: "1"
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      // console.log(key, keyPath);
      if (keyPath == 1) {
        this.$router.push({ name: "Apply" });
      }
      // if (key == 2) {
      //   this.$router.push({ name: "property" });
      // }
      if (key == 3) {
        this.$router.push({ name: "Admission" });
      }
      // if (key == 4) {
      //   this.$router.push({ name: "equipment" });
      // }
      // if (key == 5) {
      //   this.$router.push({ name: "greenshcoll" });
      // }
      // if (key == 6) {
      //   this.$router.push({ name: "stop" });
      // }
      // if (key == 7) {
      //   this.$router.push({ name: "work" });
      // }
    }
    // rout(index){
    //   if(index==1){
    //     this.$router.push({ name: "home" });
    //   }
    // }
  }
};
</script>
<style lang="less">
#bg-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  position: fixed;
  height: 80px;
  top: 40px;
  left:0;
  z-index: 10;
  width: 100%;
  color: #8791a2;
  background: #0a2549;
}
#logo{
  position: fixed;
  top:0;
  background-color: #fff;
  z-index: 10;
  width: 100%;
  h3{
    float: right;
    margin-right: 40px;
    line-height: 10px;
  }
}
.pty{
  width: 90px;
  height: 50px;
  float: left;
}
.righ{
  z-index: 11;
  float: right;
  margin-right: 60px;
}
.time{
  line-height: 40px;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
