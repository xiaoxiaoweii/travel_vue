<template>
    <div class="area">
      <div class="title">字母排序</div>
      <div
        class="gene-list letter-list"
        v-for="(item, key) of cities"
        :key="key"
        @click="handleLetterClick"
      >
        {{key}}
    </div>
</template>

<script>
export default {
  name: 'CityList',
  mpunted () {
    this.scroll = new Bscroll(this.$refs.wrapper)
  },
  props: {
    hot: Array,
    cities: Object,
    letter: String
  },
  methods: {
    handleLetterClick (e) {
      this.$emit('change', e.target.innerText)
    }
  },
  watch: {
    letter() {
      if(this.letter) {
        const element = this.$ref[this.letter][0]
        this.scroll.scrollToElement(element)
      }
    }
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
