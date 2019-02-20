<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
        <div class="title border-topbottom">当前城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">热门城市</div>
        <div class="button-list">
          <div class="button-wrapper" v-for="item of hotCities" :key="item.id">
            <div class="button">{{item.name}}</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">字母排序</div>
        <div class="alphabet-list">
          <div class="alphabet-item" v-for="(item, key) of cities" :key="key">
            {{key}}
          </div>
        </div>
      </div>
      <div class="area" v-for="(item, key) of cities" :key="key">
        <div class="title border-topbottom">{{key}}</div>
        <div class="item-list">
          <div class="item border-bottom" v-for="innerItem of item" :key="innerItem.id">
            {{innerItem.name}}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CityList',
  props: {
    cities: Object,
    hotCities: Array
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.wrapper)
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variable.styl'
  .border-topbottom
    &:before
      border-color: #ccc
    &:after
      border-color: #ccc
  .border-bottom
    &:before
      border-color: #ccc
    &:after
      border-color: #ccc
  .list
    top: 1.58rem
    left: 0
    right: 0
    bottom: 0
    position: absolute
    overflow: hidden
    .title
      color: #666
      line-height: 0.54rem
      background: #eee
      padding-left: 0.2rem
      font-size: 0.26rem
    .button-list
      overflow: hidden
      padding: 0.1rem 0.1rem
      .button-wrapper
        width: 33.3%
        float: left
        .button
          margin: 0.1rem
          padding: 0.1rem 0
          text-align: center
          border: 0.02rem solid #ccc
          border-radius: 0.06rem
    .alphabet-list
      overflow: hidden
      padding-top: 0.2rem
      .alphabet-item
        line-height: 0.66rem
        color: #666
        text-align: center
        width: 16.66%
        float: left
    .item-list
      .item
        line-height: 0.76rem
        padding-left: 0.2rem
</style>
