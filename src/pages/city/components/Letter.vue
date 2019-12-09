<template>
    <div class="list">
      <div class="area">
        <div class="title">字母排序</div>
        <div 
          class="letter-list"
          v-for="(item, key) of cities"
          :key="key"
        >
          {{key}}
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'CityLetter',
  props: {
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
    .letter-list
      box-sizing: border-box
      float: left
      height: .8rem
      width: 16.66%
      line-height: .8rem
      text-align: center
      background: #fff
      ellipsis()  
</style>
