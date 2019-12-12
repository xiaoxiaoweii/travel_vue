<template>
  <div class="around">
    <span class="around-left border-rightleft">
      <em class="iconfont around-icon">&#xe61b;</em>
      附近
    </span>
    <span class="around-left">
      <em class="iconfont around-icon">&#xe630;</em>
      必游清单
    </span>
  </div>
</template>

<script>
export default {
  name: 'HomeAround'
}
</script>

<style lang="stylus" scoped>
  .border-rightleft
    &:before
      border-color: #ffe
    &:after
      border-color: #212121
  .around
    display: flex
    line-height: 1rem
    background: #fff
    .around-left
        margin: .1rem 0
        width: 50%
        float: left
        text-align: center
        .around-icon
          color: #616161
</style>
