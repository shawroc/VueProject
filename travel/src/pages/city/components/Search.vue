<template>
  <div>
    <div class="search">
      <input v-model="keyWord" class="search-input" type="text" placeholder="输入城市名或者拼音">
    </div>
    <div class="search-content" ref="search" v-show="keyWord">
      <ul>
        <li class="search-item border-bottom" v-for="item of list" :key="item.id" @click="handlerCityClick(item.name)">{{item.name}}</li>
        <li class="search-item border-bottom" v-show="hasNoData">没有找到匹配数据</li>
      </ul>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CitySearch',
  props: {
    cities: Object
  },
  data () {
    return {
      keyWord: '',
      list: [],
      timer: null
    }
  },
  methods: {
    handlerCityClick (city) {
      this.$store.commit('changeCity', city)
      this.$router.push('/')
    }
  },
  watch: {
    keyWord () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      if (!this.keyWord) {
        this.list = []
        return
      }
      this.timer = setTimeout(() => {
        const result = []
        for (let i in this.cities) {
          this.cities[i].forEach((value) => {
            if (value.spell.indexOf(this.keyWord) > -1 || value.name.indexOf(this.keyWord) > -1) {
              result.push(value)
            }
          })
        }
        this.list = result
      }, 100)
    }
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.search)
  },
  computed: {
    hasNoData () {
      return !this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variable.styl'
  .search
    height: 0.72rem
    padding: 0 0.1rem
    background-color: $bgColor
    .search-input
      box-sizing: border-box
      width: 100%
      height: 0.62rem
      line-height: 0.62rem
      color: #666
      text-align: center
      border-radius: 0.06rem
      padding: 0 0.2rem
  .search-content
      position: absolute
      top: 1.58rem
      left: 0
      right: 0
      bottom: 0
      overflow: hidden
      background: #fff
      z-index: 1
      .search-item
        line-height: 0.62rem
        padding-left: 0.2rem
        color: #666
</style>
