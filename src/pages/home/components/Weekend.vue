<template>
  <div class="recommend">
    <div class="title">
      周末去哪儿
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
        <p class="info">{{item.title}}</p>
        <p class="info item-desc">{{item.desc}}</p>
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
  @import '~styles/mixins.styl';
  .recommend
    background: #fff
    .title
      line-height: .8rem
      font-size: 0.32rem
      text-indent: .2rem
      background: #f5f5f5
    .item-img-wrapper
      overflow: hidden
      height: 0
      padding-bottom: 35%
      .item-img
        width: 100%
    .info
      margin: .16rem
      padding: 0 1.4rem 0 0
      ellipsis()
    .item-desc
      font-size: .24rem
      color: #616161
</style>
