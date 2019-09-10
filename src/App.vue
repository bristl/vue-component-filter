<template lang='pug'>
  #app
    <router-view/>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style lang='stylus'>
body
  margin 0
#app
  min-height 100vh
  padding-top 200px
  font-family 'Avenir', Helvetica, Arial, sans-serif
  display flex
  flex-direction column
  align-items center

  background-color #F1F1F5
</style>
