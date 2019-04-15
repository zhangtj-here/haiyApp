<template>
  <div id="container" :style="{backgroundImage: 'url(' + img + ')' }">
    <img class="logo" src="@/assets/logocnodc.png">
    <el-row id="formRow">
      <el-col :span="24">
        <el-form ref="form" :model="form" >
          <el-form-item label="">
            <el-input
              placeholder="请输入用户名"
              v-model="form.name"
              clearable>
            </el-input>
          </el-form-item>
          <el-form-item label="">
            <el-input
              placeholder="请输入密码"
              type="password"
              v-model="form.password"
              clearable>
            </el-input>
          </el-form-item>
          <el-button type="primary" @click="goHome" id="login">登录</el-button>
        </el-form>
      </el-col>
    </el-row>
  </div>
</template>
<script>
import Img from '@/assets/7.jpg'

export default {
  data () {
    return {
      img: Img,
      form: {
        name: '',
        password: ''
      }
    }
  },
  methods: {
    goHome () {
      const self = this
      // alert('invitaue user or password')
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
  #formRow{
    padding: 0 10px;
    margin-top: 20px;
  }
  #login{
    width: 100%;
  }
</style>
