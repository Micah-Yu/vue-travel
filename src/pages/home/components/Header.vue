<template>
<div class="header">
  <div class="header-left">
    <div class="iconfont back-icon">&#xe658;</div>
  </div>
  <div class="header-input">
    <span class="iconfont">&#xe720;</span>
    输入城市/景点/游玩主题
  </div>
  <router-link to="/city">
    <div class="header-right">
      {{this.city}}
      <span class="iconfont">&#xe65c;</span>
    </div>
  </router-link>
</div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .header
    display flex
    line-height $headerHeight
    background-color $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        text-align center
        font-size .6rem
    .header-input
      flex: 1
      height .62rem
      line-height .62rem
      margin-top .12rem
      margin-left .2rem
      padding-left .2rem
      background #ffffff
      border-radius .1rem
      color: #ccc
    .header-right
      min-width 1.04rem
      padding 0 .1rem
      float: right
      color #fff
      text-align center
</style>
