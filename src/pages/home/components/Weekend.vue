<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of list"
        :key="item.id"
      >
        <div class="item-img-wrapper">
          <img class="item-img" :src='item.imgUrl' alt="">
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
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped >
  @import './../../../assets/style/mixins.styl'
  .title
    background #eee
    text-indent .2rem
    line-height .8rem
  .item-img-wrapper
    height 0
    padding-bottom 37.09%
    overflow hidden
    .item-img
      width 100%
  .item-title
    font-size .32rem
    line-height .54rem
    ellipse()
  .item-desc
    line-height .4rem
    color #ccc
    ellipse()
</style>
