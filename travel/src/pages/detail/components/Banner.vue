<template>
  <div>
    <div class="banner" @click="handlerBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1502/a3/a32318f0ec732f35.water.jpg_600x330_4c17874d.jpg" alt=""/>
      <div class="banner-info">
        <div class="banner-title">大连圣亚海洋世界</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe692;</span>
          39
        </div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handlerGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1501/f7/f764fb7d44427c07.water.jpg_r_800x800_8b1ed1f9.jpg', 'http://img1.qunarzz.com/sight/p0/1502/27/2729ca6f3012a380.water.jpg_r_800x800_5983e483.jpg']
    }
  },
  methods: {
    handlerBannerClick () {
      this.showGallary = true
    },
    handlerGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      color: #fff
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: 0.6rem
      background-image: linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,0.8))
      .banner-title
        flex: 1
        font-size: 0.32rem
        padding: 0 0.2rem
      .banner-number
        height: 0.4rem
        line-height: 0.4rem
        margin-top: 0.14rem
        margin-right: 0.14rem
        font-size: 0.24rem
        padding: 0 0.32rem
        border-radius: 0.2rem
        background: rgba(0,0,0,0.8)
        .banner-icon
          font-size: 0.24rem
</style>
