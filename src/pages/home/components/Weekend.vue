<template>
  <div class="weekend">
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <div class="item-wrapper">
          <div class="item-img-wrapper">
            <img class="item-img" :src="item.imgUrl" alt="">
          </div>
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    line-height: .8rem
    font-size: .3rem
    background: #eee
    text-indent: .2rem
    margin-top: .3rem
  .item-wrapper
    .item-img-wrapper
      height: 0
      overflow: hidden
      padding-bottom: 37.06%
      .item-img
        width: 100%
    .item-info
      padding: .1rem .2rem
      .item-title
        line-height: .6rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .55rem
        color: #aaa
        ellipsis()
</style>
