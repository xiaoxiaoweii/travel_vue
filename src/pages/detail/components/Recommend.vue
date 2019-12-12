<template>
  <div class="recommend">
    <div class="title">
      看了该景点的人还看了
    </div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of list"
        :key="item.id"
      >
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-discuss">
            <span class= "iconfont left"><em>&#xe600;&#xe600;&#xe600;&#xe600;&#xe600;&#xe600;</em></span>
            <span class="right">{{item.discuss}}条评论</span>
          </p>
          <p class="item-price">
            <span>
              <em class="price-icon">￥</em>
              <em class="price-number">{{item.number}}</em>
              <em class="price-end">起</em>
            </span>
            <span class="item-place">{{item.place}}</span>
          </p>
        </div>
      </li>
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
    .recommend
      background: #fff
    .title
      margin-top: .2rem
      line-height: .8rem
      font-size: 0.32rem
      text-indent: .2rem
      .title-icon
        color: #FF6347
    .item
      overflow: hidden
      display: flex
      height: 2.4rem
      .item-img
        width: 2.2rem
        height: 2.2rem
        padding: .1rem
      .item-label
        position: absolute
        margin: .1rem
        top: 0
        left: 0
        height: .4rem
        width: 1rem
        border-radius: 0 0 0.2rem 0
        line-height: .38rem
        background: #ffa116
        font-size: .24rem
        color: #ffffff
      .item-info
        flex: 1
        padding: .1rem
        .item-title
          margin-top: .26rem
          line-height: .6rem
          font-size: .32rem
        .item-discuss
          margin-top: .06rem
          line-height: .4rem
          color: #616161
          .left
            float: left
            width: 1.5rem
            letter-spacing: -.15rem
            color: #FFB436
        .item-price
          margin-top: .22rem
          .price-icon
            font-size: .24rem
            color: #FF8300
          .price-number
            margin-left: -.1rem
            font-size: .40rem
            color: #FF8300
          .price-end
            margin-left: -.05rem
          .item-place
            float: right
            margin-right: .1rem
            line-height: .4rem
            font-size: .24rem
</style>
