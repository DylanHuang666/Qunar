<template>
  <div class="detail">
    <detail-banner :sightName="sightName" :bannerImg="bannerImg" :gallaryImgs="gallaryImgs"></detail-banner>
    <detail-header :name="name"></detail-header>
    <div class="content">
      <detail-list :list="list"></detail-list>
    </div>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
import axios from 'axios'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  methods: {
    getDetailInfo () {
      axios.get('/Qunar/static/mock/detail.json', {
        params: {
          id: this.$route.params.id
        }
      }).then(this.handleGetDataSucc)
    },
    handleGetDataSucc (res) {
      if (res.data.ret && res.data.data) {
        this.sightName = res.data.data.sightName
        this.bannerImg = res.data.data.bannerImg
        this.gallaryImgs = res.data.data.gallaryImgs
        this.list = res.data.data.categoryList
        this.name = res.data.data.name
      }
    }
  },
  mounted () {
    this.getDetailInfo()
  },
  data () {
    return {
      name: '',
      sightName: '',
      bannerImg: '',
      gallaryImgs: [],
      list: []
    }
  }
}
</script>

<style lang="stylus" scoped>
  .content
    height: 50rem
</style>
