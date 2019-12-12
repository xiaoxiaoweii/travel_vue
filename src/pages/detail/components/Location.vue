<template>
  <div class="location">
    <em class="iconfont around-icon">&#xe61b;</em>
    <span class="info">江苏省南京市江宁区银杏湖大道520号</span>
    <em class="iconfont around-icon">&#xe62c;</em>
  </div>
</template>

<script>
export default {
  name: 'DetailLocation'
}
</script>

<style lang="stylus" scoped>
  .location
    display: flex
    height: .5rem
    line-height: .5rem
    .info
      width: 90%
    .around-icon
      flex: 1
</style>
