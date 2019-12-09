<template>
    <div class="list">
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
       <div class="area">
        <div class="title">字母排序</div>
        <div 
          class="gene-list letter-list"
          v-for="(item, key) of cities"
          :key="key"
        >
          {{key}}
        </div>
      </div>
      <div 
        class="area" 
        v-for="(item, key) of cities"
        :key="item.id"
      >
        <div class="title">{{key}}</div>
        <div 
          class="gene-list city-list"
          v-for="innerItem of item"
          :key="innerItem.id"
        >
          {{innerItem.name}}</div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'CityList',
  props: {
    hot: Array,
    cities: Object
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
    .gene-list
      box-sizing: border-box
      float: left
      height: .8rem
      line-height: .8rem
      text-align: center
      background: #fff
      ellipsis()
    .hot-list
      width: 33.33%
      border: .01rem solid #ddd
    .letter-list
      width: 16.66%
    .city-list
      width: 25%
      border: .01rem solid #ddd
</style>
