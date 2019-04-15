<template>
  <div id="container" :style="{backgroundImage: 'url(' + img + ')' }">
    <img class="logo" src="@/assets/logocnodc.png">
    <mt-field label="用户名" placeholder="请输入用户名" v-model="username"></mt-field>
    <mt-field label="密码" placeholder="请输入密码" type="password" v-model="password"></mt-field>
    <mt-button type="primary" size="large" class="login_button" @click="goHome">登录</mt-button>
  </div>
</template>
<script>
import Img from '@/assets/7.jpg'

export default {
  data () {
    return {
      img: Img,
      username: '',
      password: '',
      form: {
        name: '',
        password: ''
      }
    }
  },
  methods: {
    goHome () {
      const self = this
      self.$router.push('/home')
    }
  }
}
</script>

<style scoped>
  div#container{
    height: 100%;
    padding-top: 30px;
    background-position: center center;
    background-repeat:  no-repeat;
    background-size: auto 100%;
    box-sizing: border-box;
  }
  .logo{
    width: 150px;
  }
  .login_button{
    margin-top: 30px;
  }

</style>
