<template>
  <div id="app">
    <mt-header title="高德地图">
      <mt-button icon="back" slot="left" @click="goBack" >goback</mt-button>
        <!-- <mt-button @click="handleClose">close</mt-button> -->
      <mt-button icon="more" slot="right"></mt-button>
    </mt-header>
    <h3 class="title">{{ msg }}</h3>
    <div class="amap-wrapper">
      <el-amap class="amap-box" :vid="'amap-vue'"></el-amap>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Amap',
  data () {
    return {
      msg: 'vue-amap向你问好！'
    }
  },
  methods: {
    goBack () {
      this.$router.history.go(-1)
    }
  }
}
</script>

<style scoped>
  .amap-wrapper{
    width: 100%;
    height: 500px;
  }
</style>
