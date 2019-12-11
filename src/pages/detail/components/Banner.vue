<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1603/5e/5ef2033d103ec26a90.water.jpg_600x330_8beb5f35.jpg">
      <div class="banner-info">
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe71b;</span>
          39
        </div>
        <div class="banner-tittle">
          栖霞山(AAAA景区)
        </div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClose"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['//img1.qunarzz.com/sight/p0/1603/5e/5ef2033d103ec26a90.water.jpg_600x330_8beb5f35.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-number
        width: 7%
        height: .32rem
        line-height: .32rem
        margin-top: .14rem
        margin-left: .2rem
        padding: 0 .4rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
      .banner-tittle
        font-size: .32rem
        padding: 0 .2rem
</style>
