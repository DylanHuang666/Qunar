<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" alt="">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/cd67366cb7b7bda9333b9be02272f7b0.jpg_r_640x290x70_768b1307.jpg'
      },
      {
        id: '0002',
        imgUrl: 'https://tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/4968398bc8587f91bc21d30a44c3d2d8.jpg_r_640x290x70_e0162260.jpg'
      },
      {
        id: '0003',
        imgUrl: 'https://tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/6bd6c4f555472ddbad0bdaab53b0ca44.jpg_r_640x290x70_d1a74869.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    width: 100%
    height: 0
    overflow: hidden
    padding-bottom: 48%
    background: #eee
    .swiper-img
      width: 100%
      height: 180px
</style>
