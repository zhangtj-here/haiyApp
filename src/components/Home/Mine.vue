<template>
  <div>
    <mt-header title="我的">
      <router-link to="/" slot="left">
        <!--<mt-button icon="back">返回</mt-button>-->
      </router-link>
      <!--<mt-button icon="more" slot="right"></mt-button>-->
    </mt-header>
    <div style="padding: 10px;">
      <img src="@/assets/logo.png" alt="" style="height: 50px;float: left;margin-right: 10px;">
      <div>李红</div>
      <div>科技信息部</div>
    </div>
    <mt-cell title="域名" icon="success" style="margin-top: 50px;">
      <!--<img slot="icon" src="@/assets/logo.png" width="24" height="24">-->
    </mt-cell>
    <mt-cell title="账号" icon="success">
      <!--<img slot="icon" src="@/assets/logo.png" width="24" height="24">-->
    </mt-cell>
    <mt-button type="default" size="large" style="margin-top: 50px;">绑定</mt-button>
    <mt-button type="default" size="large" style="margin-top: 10px" @click="layout">退出登录</mt-button>
  </div>
</template>

<script>
export default {
  name: 'Mine',
  methods: {
    layout () {
      const self = this
      self.$router.push('/Login')
    }
  }
}
</script>

<style scoped>

</style>
