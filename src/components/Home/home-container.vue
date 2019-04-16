<template>
  <div>
    <mt-header title="oa移动办公">
      <router-link to="/" slot="left">
      </router-link>
    </mt-header>
    <div id="topLink">
      <div>
        <img src="@/assets/logo.png" alt="">
        111
      </div>
      <div>
        <img src="@/assets/logo.png" alt="">
        222
      </div>
      <div>
        <img src="@/assets/logo.png" alt="">
        222
      </div>
      <div>
        <img src="@/assets/logo.png" alt="">
        222
      </div>
      <div>
        <img src="@/assets/logo.png" alt="">
        222
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'home-container',
  props: {
    title: String
  }
}
</script>

<style scoped>
  #topLink{
    display: flex;
    flex-flow: row  nowrap;
  }
  #topLink div{
    display: flex;
    flex: auto;
    flex-direction: column;
    height: 100px;
    align-items: center;
    justify-content: center;
  }
  #topLink div img{
    height: 60px;
  }
</style>
