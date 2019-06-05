<template>
  <ul class="alphabet">
    <li class="item" v-for="(item,key) of cities" :key="key">{{key}}</li>
  </ul>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: {
    cities: Object
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .alphabet
    position: absolute
    top: 1.58rem
    right: 0
    bottom: 0
    width: .4rem
    text-align: center
    display: flex
    flex-direction: column
    justify-content: center
    .item
      line-height: .4rem
      color: $bgColor
</style>
