<template>
  <div>
      <router-link
      tag="div"
      class="header-abs"
      v-show="showAbs"
      to="/">
        <span class="iconfont header-abs-header">&#xe624;</span>
      </router-link>
      <div class="header-fixed"
      v-show="!showAbs"
      :style="opacityStyle"
      >
        <router-link to="/">
          <div class="iconfont header-fixed-back">&#xe624;</div>
        </router-link>
        景点详情
      </div>
  </div>
</template>

<script>
export default {
  name: 'DetailHeader',
  data () {
    return {
      showAbs: true,
      opacityStyle: {
        opacity: 0
      }
    }
  },
  methods: {
    handlerScroll () {
      const top = document.documentElement.scrollTop
      if (top > 60) {
        let opacity = top / 140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = {opacity}
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
  },
  activated () {
    window.addEventListener('scroll', this.handlerScroll)
  },
  deactivated () {
    window.removeEventListener('scroll', this.handlerScroll)
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/variable.styl'
  .header-abs
    position: absolute
    left: 0.2rem
    top: 0.2rem
    width: 0.8rem
    height: 0.8rem
    border-radius: 50%
    text-align: center
    line-height: 0.8rem
    background: $bgColor
    .header-abs-header
      color: #fff
      font-size: 0.4rem
  .header-fixed
    height: $headerHeight
    line-height: $headerHeight
    font-size: 0.32rem
    overflow: hidden
    text-align: center
    color: #fff
    background-color: $bgColor
    top: 0
    left: 0
    right: 0
    position: fixed
    .header-fixed-back
      color: #fff
      width: 0.64rem
      text-align: center
      font-size: 0.4rem
      top: 0
      left: 0
      position: absolute
</style>
