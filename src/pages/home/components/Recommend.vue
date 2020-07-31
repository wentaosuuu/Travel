<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <router-link
        tag="li"
        class="item border-bottom"
        v-for="item of list"
        :key="item.id"
        :to="'/detail/' + item.id"
      >
        <img class="item-img" :src='item.imgUrl' alt="">
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
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import './../../../assets/style/mixins.styl'
  .title
    background #eee
    text-indent .2rem
    margin-top .2rem
    line-height .8rem

  .item
    overflow hidden
    display flex
    height 1.9rem

    .item-img
      padding .1rem
      height 1.7rem
      width 1.7rem

    .item-info
      padding .1rem
      flex 1
      min-width 0

    .item-title
      font-size .32rem
      line-height .54rem
      ellipse()

    .item-desc
      line-height .4rem
      color #ccc
      ellipse()

    .item-button
      padding .1rem
      margin-top .16rem
      border-radius .06rem
      line-height .44rem
      color #fff
      background #ff9300
</style>
