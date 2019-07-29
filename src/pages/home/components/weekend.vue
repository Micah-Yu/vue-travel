<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="图片">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/e3/e9761259adfc1d.jpg_r_640x214_21b96532.jpg',
        title: '哈尔滨必游',
        desc: '冰雪之冠，富有异国情调的美丽都市'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9d/289843ecff0d03.jpg_r_640x214_931d3e12.jpg',
        title: '避暑好去处',
        desc: '哈尔滨的美不只在冬日，夏日更惬意'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/91/04b59ae6faf17a.jpg_r_640x214_ce69a65a.jpg',
        title: '东方小巴黎的魅力',
        desc: '中央大街随处可见的西式文化你想探个究竟吗？来这里感受文艺复兴风格的建筑'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item
    border #25a4bb solid 1px
    margin .04rem 0
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 33.9%
    .item-img
      width 100%
  .item-info
    padding .2rem
    .item-title
      line-height .54rem
      ellipse()
    .item-desc
      line-height .4rem
      color #777
      ellipse()
</style>
