<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1512/51/5193b969b371d76990.water.jpg_600x330_99d01917.jpg" alt="pic">
      <div class="banner-info">
        <div class="banner-title">哈尔滨极地馆(AAAA景区)</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe614;</span>
          12
        </div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  components: {
    CommonGallary
  },
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1512/51/5193b969b371d76990.water.jpg_r_800x800_41b63c4d.jpg', 'http://img1.qunarzz.com/sight/p0/1810/bc/bc175fe029d11757a3.img.jpg_r_800x800_8a1361b5.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      display flex
      position absolute
      left 0
      right 0
      bottom 0
      line-height .6rem
      color #fff
      background-image linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,0.6))
      .banner-title
        flex 1
        font-size .32rem
        padding 0 .2rem
      .banner-number
        height .32rem
        margin-top .14rem
        padding 0 .4rem
        line-height .32rem
        border-radius .2rem
        background rgba(0, 0, 0, .5)
        font-size .24rem
        .banner-icon
          font-size .24rem
</style>
