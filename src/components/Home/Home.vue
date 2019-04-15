<template>
  <el-container :horizontal="horizontal">
    <el-header>Header</el-header>
    <el-main>
      <el-tabs :tab-position="tabPosition" style="height: 100%;" :stretch="stretch">
        <el-tab-pane label="首页">
          <homeContainer title="首页"></homeContainer>
        </el-tab-pane>
        <el-tab-pane label="待办">
          <homeContainer title="配置管理"></homeContainer>
        </el-tab-pane>
        <el-tab-pane label="我的">
          <homeContainer title="定时任务补偿"></homeContainer>
        </el-tab-pane>
      </el-tabs>
    </el-main>
    <el-footer id="footer">
      <el-row>
        <el-col :span="8">
          <div class="grid-content">
            <img src="@/assets/logo.png" alt="" style="width: 10px;">
            <div>首页</div>
          </div>
        </el-col>
        <el-col :span="8"><div class="grid-content">2</div></el-col>
        <el-col :span="8"><div class="grid-content">3</div></el-col>
      </el-row>
    </el-footer>
  </el-container>
</template>

<script>
import homeContainer from './home-container'
export default {
  name: 'Home',
  data () {
    return {
      tabPosition: 'bottom',
      stretch: true
    }
  },
  components: {
    homeContainer
  }
}
</script>

<style scoped>
#tab_one{
  /*width: 100%;*/
  height: 20rem;
  background: red;
}
#footer{
  position: absolute;
  width: 100%;
  bottom: 0;
}
</style>
