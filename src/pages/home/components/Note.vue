<template>
  <div class="note">
    <span class="iconfont note-icon">&#xe63d;</span>
    <span class="note-content"><em class="note-title">票面价</em>是指通过景区指定窗口售卖的纸质门票上标注的价格</span>
  </div>
</template>

<script>
export default {
  name: 'HomeNote'
}
</script>

<style lang="stylus" scoped>
  .note
    margin-top: .2rem
    background: #fff
    .note-icon
      margin-left: .2rem
      font-size: .24rem
    .note-content
      height: .6rem
      line-height: .6rem
      font-size: .24rem
      .note-title
        font-weight: 700
</style>
