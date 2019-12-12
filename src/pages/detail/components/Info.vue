<template>
  <div class="info">
    <span class="info-left border-rightleft">
      <span class="left discuss">
        <em class="number">5.0</em>
        分&nbsp;超赞</span>
      <em class="iconfont around-icon">&#xe62c;</em>
    </span>
    <span class="info-left">
      <span class="left introduce">景点简介</span>
      <em class="iconfont around-icon">&#xe62c;</em>
    </span>
  </div>
</template>

<script>
export default {
  name: 'DetailInfo'
}
</script>

<style lang="stylus" scoped>
  .border-rightleft
    &:beforeleft
      border-color: #ffe
    &:after
      border-color: #212121
  .info
    display: flex
    line-height: 1rem
    background: #fff
    .info-left
      display: flex
      margin: .1rem 0
      width: 50%
      float: left
      text-align: center
      .left
        width: 70%
      .discuss
        color: #ff8300
        .number
          font-size: .4rem
      .around-icon
        padding-left: .75rem
        flex: 1
        color: #616161
</style>
