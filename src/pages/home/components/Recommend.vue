<template>
  <div class="recommend">
    <div class="title">热销推荐</div>
    <ul>
      <router-link tag="li" :to="'/detail/' + item.id" class="item border-bottom" v-for="item of list" :key="item.id">
        <div class="item-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button class="item-button">查看详情</button>
          </div>
        </div>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    line-height: .8rem
    font-size: .3re
    background: #eee
    text-indent: .2rem
    margin-top: .3rem
  .item-wrapper
    display: flex
    padding: .2rem .05rem
    .item-img
      width: 2rem
      height: 2rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .65rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .55rem
        color: #aaa
        ellipsis()
      .item-button
        padding: .03rem .2rem
        background: #ff9300
        line-height: .44rem
        color: #fff
        border-radius: .08rem
        margin-top: .15rem
</style>
