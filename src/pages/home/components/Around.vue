<template>
  <div class="around">
    <span class="around-left border-bottom">
      <em class="iconfont around-icon">&#xe61b;</em>
      附近
    </span>
    <span class="around-left border-bottom">
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
  .around
    display: flex
    line-height: 1rem
    background: #fff
    .around-left
        width: 50%
        float: left
        text-align: center
        .around-icon
          color: #616161
</style>
