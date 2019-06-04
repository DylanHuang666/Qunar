<template>
  <div class="recommend">
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button class="item-button">查看详情</button>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
        title: '故宫',
        desc: '世界五大宫之首，穿越与您近在咫尺'
      },
      {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1708/2b/2b3b94de99c0a425a3.img.jpg_200x200_2458ffb2.jpg',
        title: '八达岭长城',
        desc: '不到长城非好汉'
      },
      {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg',
        title: '北京欢乐谷',
        desc: '亚洲唯一飞行式过山车等你来挑战'
      },
      {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1507/36/ce3d2d6c9ab44d67ae68d940b8781829.water.jpg_200x200_0938a8f2.jpg',
        title: '北京野生动物园',
        desc: '敢与森林之王近距离接触吗？'
      }]
    }
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
