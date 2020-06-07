<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of RecommendList"
        :key="item.id"
      >
        <img class="item-img" :src='item.imgURL' alt="">
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
      RecommendList: [{
        id: '0001',
        imgURL: 'http://img1.qunarzz.com/sight/p0/1507/cc/19733fc0135062788140cbb48ae606a7.water.jpg_200x200_d9ebe2fd.jpg',
        title: '大连东北虎',
        desc: '凶残凶残东北虎'
      }, {
        id: '0002',
        imgURL: 'http://img1.qunarzz.com/sight/p0/1507/cc/19733fc0135062788140cbb48ae606a7.water.jpg_200x200_d9ebe2fd.jpg',
        title: '大连东北虎',
        desc: '凶残凶残东北虎'
      }, {
        id: '0003',
        imgURL: 'http://img1.qunarzz.com/sight/p0/1507/cc/19733fc0135062788140cbb48ae606a7.water.jpg_200x200_d9ebe2fd.jpg',
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
