<template>
<div>
  <div class="title">热销推荐</div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
      <img class="item-img" :src="item.imgUrl" alt="图片">
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
      recommendList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1512/51/5193b969b371d76990.water.jpg_200x200_b4c5e77f.jpg',
        title: '哈尔滨极地馆',
        desc: '"极地鲸灵炫乐团” 倾力领衔“鲸”彩绝伦的七大主题表演'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1803/5b/5b0254406105ac85a3.img.jpg_200x200_e7c0be01.jpg',
        title: '伏尔加庄园',
        desc: '踏上幸福桥远眺的那一刻，人们的目光自然而然的会落在这座雄浑美丽的城堡之上。'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1905/52/52eceacd843304d8a3.img.jpg_200x200_44d998c0.jpg',
        title: '波塞冬沙滩水世界',
        desc: '穿越小美人鱼岛蜿蜒的水线，踏入奇幻的海底世界，玄妙的海洋之旅随即展开，小美人鱼公主期待与你奇遇哦！\n' +
          '小美人鱼岛的所有项目都是为儿童量身打造，小朋友们在这里可以尽情享受亲水的无限欢乐。'
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
    overflow hidden
    display flex
    height 1.9rem
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .54rem
        font-size .32rem
        ellipse()
      .item-desc
        line-height .4rem
        color #ccc
        ellipse()
      .item-button
        line-height .44rem
        margin-top .2rem
        background: #ff9300
        padding 0 .2rem
        border-radius .6rem
        color #fff
</style>
