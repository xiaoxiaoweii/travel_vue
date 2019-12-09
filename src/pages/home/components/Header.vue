<template>
    <div class="header">
      <div class="header-left">
        <div class="iconfont back-icon">&#xe601;</div>
      </div>
      <div class="header-input">
        <span class="iconfont">&#xe64c;</span>
        输入城市/景点/游玩主题
      </div>
      <router-link to='/city'>
        <div class="header-right">
          {{this.city}}
          <span class="iconfont arrow-icon">&#xe606;</span>
        </div>
      </router-link>
    </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/variables.styl';
    .header
      display: flex
      line-height: .86rem
      background: $bgColor
      color: #ffffff
      .header-left
        width: .64rem
        float: left
        .back-icon
          text-align: center
          font-size: .2rem
      .header-input
        flex: 1
        height: .64rem
        line-height: .64rem
        margin-top: .12rem
        margin-left: .2rem
        padding-left: .2rem
        background: #ffffff
        border-radius: .1rem
        color: #cccccc
      .header-right
        width: 1.24rem
        float: right
        text-align: center
        color: #fff
        .arrow-icon
          margin-left: -.04rem
          font-size: .2rem
</style>
