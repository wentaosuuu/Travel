<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgURL" alt="">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgURL: 'https://t8.baidu.com/it/u=1904929927,2760345427&fm=193'
      }, {
        id: '0002',
        imgURL: 'https://t7.baidu.com/it/u=2543309874,4285392330&fm=193'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper
    overflow: hidden
    width: 100%
    height :  0
    padding-bottom:31.25%
    background #333333
    .swiper-img
      width: 100%
</style>
