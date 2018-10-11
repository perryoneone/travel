<template>
  <div class='wraper'>
    <swiper :options="swiperOption">
        <!-- slides -->
        <swiper-slide v-for='item of swiperList' :key=item.id>
            <img class='swiper-img' :src=item.imgUrl />
        </swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: '001',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1809/c6/2467595fffc3b302.jpg_750x200_cca13d51.jpg'
        },
        {
          id: '002',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1801/bd/04554e7c67650302.jpg_750x200_4293d60a.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
    .wraper >>> .swiper-pagination-bullet-active
        background-color: #fff
    .wraper
        overflow: hidden
        width: 100%
        height: 0
        padding-bottom: 26.67%
        background-color: #eee
        .swiper-img
            width: 100%
</style>
