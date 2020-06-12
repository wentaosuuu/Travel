<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe602;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe612;</span>
      输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont arrow-icon">&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
  @import '~style/varibles.styl'
  .header
    display:flex
    line-height: $headerHeight
    background:$bgColor
    color:#fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        text-align: center
        font-size : .6rem
    .header-input
      flex:1
      height: .64rem
      line-height:.64rem
      margin-top: .12rem
      margin-left:.2rem
      padding-left :.2rem
      background:#fff
      border-radius:.1rem
      color:#ccc
    .header-right
      width:1.24rem
      float:right
      color #fff
      text-align: center
      .arrow-icon
        font-size: .24rem
</style>
