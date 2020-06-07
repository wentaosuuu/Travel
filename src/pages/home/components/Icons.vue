<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div
          class="icon"
          v-for="item of page"
          :key="item.id"
        >
          <div class="icon-img">
            <img class="icon-img-content" :src='item.imgURL' alt="">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [{
        id: '0001',
        imgURL: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: '0002',
        imgURL: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
        desc: '一日游'
      }, {
        id: '0003',
        imgURL: 'http://img1.qunarzz.com/piao/fusion/1803/4c/eac47dd8def8de02.png',
        desc: '北京园博园'
      }, {
        id: '0004',
        imgURL: 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
        desc: '故宫'
      }, {
        id: '0005',
        imgURL: 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
        desc: '圆明园'
      }, {
        id: '0006',
        imgURL: 'http://img1.qunarzz.com/piao/fusion/1803/67/9a1678221b8e0e02.png',
        desc: '古水北镇'
      }, {
        id: '0007',
        imgURL: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png',
        desc: '香山公园'
      }, {
        id: '0008',
        imgURL: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png',
        desc: '凤凰岭'
      }, {
        id: '0009',
        imgURL: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png',
        desc: '凤凰岭'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "./../../../assets/style/varibles.styl"
  @import "./../../../assets/style/mixins.styl"
  .icons >>> .swiper-container
    height 0
    padding-bottom 50%

  .icon
    position relative
    overflow hidden
    width 25%
    height 0
    padding-bottom 25%
    float left

  .icon-img
    top 0
    left 0
    right 0
    bottom .44rem
    box-sizing border-box
    position absolute

  .icon-img-content
    display block
    margin 0 auto
    height 100%

  .icon-desc
    left 0
    right 0
    bottom 0
    line-height .44rem
    height .44rem
    color $darkTextColor
    text-align center
    ellipse()
    position absolute
</style>
