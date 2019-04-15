<template>
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
</style>
