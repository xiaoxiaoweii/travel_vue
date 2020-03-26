<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <detail-info></detail-info>
    <detail-location></detail-location>
    <detail-recommend :list="recommendList"></detail-recommend>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailInfo from './components/Info'
import DetailLocation from './components/Location'
import DetailList from './components/List'
import DetailRecommend from './components/Recommend'
import axios from 'axios'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailInfo,
    DetailLocation,
    DetailList,
    DetailRecommend
  },
  data () {
    return {
      recommendList: []
    }
  },
  methods: {
    getDetailInfo () {
      axios.get('../../../static/api/index.json')
        .then(this.getDetailInfoSucc)
    },
    getDetailInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        console.log(res.data)
        this.recommendList = data.recommendList
      }
      console.log(this.recommendList)
    }
  },
  mounted () {
    this.getDetailInfo()
  }
}
</script>

<style lang="stylus" scoped>
</style>
