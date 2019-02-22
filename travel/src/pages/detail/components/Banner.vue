<template>
  <div>
    <div class="banner" @click="handlerBannerClick">
      <img class="banner-img" :src="bannerImg"/>
      <div class="banner-info">
        <div class="banner-title">
          {{this.sightName}}
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe692;</span>
          {{this.gallaryImgs.length}}
        </div>
      </div>
    </div>
    <common-gallary
    :imgs="gallaryImgs"
    v-show="showGallary"
    @close="handlerGallaryClose">
    </common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  props: {
    sightName: String,
    bannerImg: String,
    gallaryImgs: Array
  },
  data () {
    return {
      showGallary: false
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
