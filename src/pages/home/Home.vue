<template>
    <div class="home">
      <home-header></home-header>
      <home-swiper :list="swiperList"></home-swiper>
      <home-icons :list="iconList"></home-icons>
      <home-around></home-around>
      <home-recommend :list="recommendList"></home-recommend>
      <home-weekend :list="weekendList"></home-weekend>
      <home-note></home-note>
    </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeAround from './components/Around'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
import HomeNote from './components/Note'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeAround,
    HomeRecommend,
    HomeWeekend,
    HomeNote
  },
  data () {
    return {
      swiperList: [],
      iconList: [],
      recommendList: [],
      weekendList: []
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('../../../static/api/index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.recommendList = data.recommendList
        this.weekendList = data.weekendList
      }
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>

<style lang="stylus" scoped>
  .home
    background: #f5f5f5
</style>
