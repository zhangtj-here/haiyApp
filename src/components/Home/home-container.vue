<template>
  <div>
    <mt-header title="oa移动办公">
      <router-link to="/" slot="left">
        <!--<mt-button icon="back">返回</mt-button>-->
      </router-link>
      <!--<mt-button icon="more" slot="right"></mt-button>-->
    </mt-header>
    <div ></div>

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

</style>
