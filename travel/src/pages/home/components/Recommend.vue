<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" :alt="item.title"/>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1810/cc/cc47164357acbeb5a3.water.jpg_200x200_151f0405.jpg',
          title: '杭州云漫温泉',
          desc: '还原泡汤文化的精髓'
        }, {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1810/cc/cc47164357acbeb5a3.water.jpg_200x200_151f0405.jpg',
          title: '杭州云漫温泉',
          desc: '还原泡汤文化的精髓'
        }, {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1810/cc/cc47164357acbeb5a3.water.jpg_200x200_151f0405.jpg',
          title: '杭州云漫温泉',
          desc: '还原泡汤文化的精髓'
        }, {
          id: '0004',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1810/cc/cc47164357acbeb5a3.water.jpg_200x200_151f0405.jpg',
          title: '杭州云漫温泉',
          desc: '还原泡汤文化的精髓'
        }
      ]
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
