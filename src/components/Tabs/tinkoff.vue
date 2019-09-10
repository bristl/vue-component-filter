<template lang='pug'>
  #a
    <button v-on:click="count++">{{count}}</button>
</template>

<script>
export default {
  name: 'tinkoff',
  data () {
    return {
      count: 0
    }
  }
}
</script>

<style lang='stylus'>
</style>
