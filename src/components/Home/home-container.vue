<template>
  <div>{{title}}</div>
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
div{
  width: 20rem;
  background: red;
}
</style>
