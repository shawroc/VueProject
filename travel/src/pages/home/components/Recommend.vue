<template>
  <div>
    <div class="title">热销推荐</div>
    <ul v-if="showRecommend">
        <router-link
        tag="li"
        :to="'/detail/' + item.id"
        class="item border-bottom"
        v-for="item of recommendList"
        :key="item.id">
          <img class="item-img" :src="item.imgUrl" :alt="item.title"/>
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button class="item-button">查看详情</button>
          </div>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    recommendList: Array
  },
  computed: {
    showRecommend () {
      return this.recommendList.length
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
  .title
    line-height: 0.8rem
    background-color: #ddd
    text-indent: 0.2rem
    margin-top: 0.2rem
  .item
    display: flex
    height: 1.9rem
    overflow: hidden
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: 0.1rem
    .item-info
      flex: 1
      padding: 0.1rem
      min-width: 0
      .item-title
        line-height: 0.54rem
        font-size: 0.32rem
        ellipsis()
      .item-desc
        line-height: 0.4rem
        color: #ccc
        ellipsis()
      .item-button
        background: #ff9300
        padding: 0 0.1rem
        border-radius: 0.06rem
        margin-top: 0.2rem
        line-height: 0.44rem
        color: #fff
</style>
