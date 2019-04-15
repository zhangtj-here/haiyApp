<template>
  <!--<el-container :horizontal="horizontal">
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
  </el-container>-->
  <div id="container">

    <mt-tab-container v-model="active">
      <mt-tab-container-item id="tab-container1">
        <homeContainer></homeContainer>
      </mt-tab-container-item>
      <mt-tab-container-item id="tab-container2">
        <li  title="tab-container 2">2</li>
      </mt-tab-container-item>
      <mt-tab-container-item id="tab-container3">
        <li  title="tab-container 3">3</li>
      </mt-tab-container-item>
      <mt-tab-container-item id="tab-container4">
          <Mine></Mine>
      </mt-tab-container-item>
    </mt-tab-container>
    <mt-tabbar v-model="selected">
      <mt-tab-item id="one" @click.native.prevent="active = 'tab-container1'">
        <img slot="icon" src="@/assets/logo.png">
        首页
      </mt-tab-item>
     <!-- <mt-tab-item id="two" @click.native.prevent="active = 'tab-container2'">
        <img slot="icon" src="@/assets/logo.png">
        待办
      </mt-tab-item>
      <mt-tab-item id="three" @click.native.prevent="active = 'tab-container3'">
        <img slot="icon" src="@/assets/logo.png">
        新建
      </mt-tab-item>-->
      <mt-tab-item id="mine" @click.native.prevent="active = 'tab-container4'">
        <img slot="icon" src="@/assets/logo.png">
        我的
      </mt-tab-item>
    </mt-tabbar>
  </div>
</template>

<script>
import homeContainer from './home-container'
import Mine from './Mine'
export default {
  name: 'Home',
  data () {
    return {
      tabPosition: 'bottom',
      stretch: true,
      active: 'tab-container1',
      n: 0,
      selected: 'one'
    }
  },
  components: {
    homeContainer,
    Mine
  },
  methods: {
    layout () {
      const self = this
      self.$router.push('/Login')
    }
  }
}
</script>

<style scoped>
#container{
  text-align: left;
}

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
