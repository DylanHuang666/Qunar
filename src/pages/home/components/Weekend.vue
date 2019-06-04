<template>
  <div class="weekend">
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of weekendList" :key="item.id">
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
  data () {
    return {
      weekendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
        title: '京城周末撒欢',
        desc: '在帝都过周末，不仅仅是城中游！'
      },
      {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/7e/476589267ebb41.jpg_r_640x214_bf599709.jpg',
        title: '在帝都过周末，不仅仅是城中游！',
        desc: '德智体美劳全面发展的亲子日，这些地方该去看看…'
      },
      {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/aa/7baaf8a851d221.jpg_r_640x214_1431200f.jpg',
        title: '帝都必打卡',
        desc: '来北京必去的景点非这些地方莫属'
      },
      {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9e/21df651e19af5d.jpg_r_640x214_3ea5bb38.jpg',
        title: '寻找北京的皇城范儿',
        desc: '数百年的宫廷庙宇，至今依旧威严霸气'
      }]
    }
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
