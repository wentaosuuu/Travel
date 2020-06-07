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
        imgURL: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1591521167624&di=b186fde29f3ba14978dbf6c22f3a408c&imgtype=0&src=http%3A%2F%2Fn.sinaimg.cn%2Fsinakd20200603ac%2F213%2Fw640h373%2F20200603%2Fbd0c-iumkapw9234077.jpg'
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
