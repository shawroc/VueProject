<template>
  <div class="list">
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
        <div class="button-wrapper">
            <div class="button">北京</div>
        </div>
        <div class="button-wrapper">
            <div class="button">北京</div>
        </div>
        <div class="button-wrapper">
            <div class="button">北京</div>
        </div>
        <div class="button-wrapper">
            <div class="button">北京</div>
        </div>
        <div class="button-wrapper">
            <div class="button">北京</div>
        </div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">字母排序</div>
      <div class="alphabet-list">
        <div class="alphabet-item">A</div>
        <div class="alphabet-item">B</div>
        <div class="alphabet-item">C</div>
        <div class="alphabet-item">D</div>
        <div class="alphabet-item">E</div>
        <div class="alphabet-item">F</div>
        <div class="alphabet-item">G</div>
        <div class="alphabet-item">H</div>
        <div class="alphabet-item">I</div>
        <div class="alphabet-item">J</div>
        <div class="alphabet-item">K</div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">A</div>
      <div class="item-list">
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">A</div>
      <div class="item-list">
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">A</div>
      <div class="item-list">
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">A</div>
      <div class="item-list">
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">A</div>
      <div class="item-list">
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">A</div>
      <div class="item-list">
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
        <div class="item border-bottom">杭州</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CityList'
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
      line-height: 0.44rem
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
