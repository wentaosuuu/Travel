<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of RecommendList"
        :key="item.id"
      >
        <div class="item-img-wrapper">
          <img class="item-img" :src='item.imgURL' alt="">
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
      RecommendList: [{
        id: '0001',
        imgURL: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
        title: '大连东北虎',
        desc: '凶残凶残东北虎'
      }, {
        id: '0002',
        imgURL: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
        title: '大连东北虎',
        desc: '凶残凶残东北虎'
      }, {
        id: '0003',
        imgURL: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
        title: '大连东北虎',
        desc: '凶残凶残东北虎'
      }]
    }
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
    padding-bottom 33.9%
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
