<template>
  <div class="header">
    <router-link to="/">
      <div class="iconfont header-back">&#xe658;</div>
    </router-link>
    城市选择
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .header
    position relative
    overflow hidden
    line-height $headerHeight
    text-align center
    color #fff
    background $bgColor
    height $headerHeight
    font-size .32rem
    .header-back
      position absolute
      color #fff
      width .64rem
      text-align center
      font-size .6rem
</style>
