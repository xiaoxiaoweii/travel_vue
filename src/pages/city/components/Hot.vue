<template>
    <div class="hot">
      <div class="area">
        <div class="title">热门城市</div>
        <div
          class="gene-list hot-list"
          v-for="item of hot"
          :key="item.id"
        >
          {{item.name}}
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'CityHot',
  props: {
    hot: Array,
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl';
  @import '~styles/mixins.styl';
  .area
    overflow: hidden
    .title
      box-sizing: border-box
      margin: .24rem .3rem
      line-height: .3rem
      color: #666
    .hot-list
      box-sizing: border-box
      float: left
      height: .8rem
      width: 33.33%
      line-height: .8rem
      text-align: center
      background: #fff    
      border: .01rem solid #ddd
      ellipsis()
</style>
