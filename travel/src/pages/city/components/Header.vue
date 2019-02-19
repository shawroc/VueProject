<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="iconfont header-back">&#xe624;</div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/variable.styl'
  .header
    height: $headerHeight
    line-height: $headerHeight
    font-size: 0.32rem
    overflow: hidden
    text-align: center
    color: #fff
    background-color: $bgColor
    position： relative
    .header-back
      color: #fff
      width: 0.64rem
      text-align: center
      font-size: 0.4rem
      top: 0
      left: 0
      position: absolute
</style>
