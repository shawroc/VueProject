<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      {{this.city}}
      <span class="iconfont area-icon">&#xe64a;</span>
    </div>
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
@import '~styles/variable.styl'
  .header
    display: flex
    line-height: 0.86rem
    color: #fff
    background-color: $bgColor
    .header-left
      width: 0.64rem
      float: left
      .back-icon
        text-align: center
        font-size: 0.4rem
    .header-input
      flex: 1
      height: 0.64rem
      line-height: 0.64rem
      margin-top: 0.12rem
      margin-left: 0.2rem
      padding-left: 0.2rem
      color: #ccc
      background-color: #fff
      border-radius: 0.1rem;
    .header-right
      width: 1.24rem
      text-align: center
      float: right
      .area-icon
        font-size: 0.2rem
        margin-left: -0.04rem
</style>
