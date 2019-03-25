<template>
  <div class="wrapper">
  <swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl">
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
  export default {
    name: 'HomeSwiper',
    data (){
      return{
        swiperOption:{
          pagination:'.swiper-pagination',
          loop: true//使轮播图可以循环轮播
        },
        swiperList: [{
          id:'0001',
          imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/bd0af35db8de5fff3379cc082fd21db6.jpg_750x200_5ea5bcce.jpg'
        },{
          id:'0002',
          imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1609/e8/a26190adcdc51c02.jpg_750x200_c4691cbe.jpg'
        }]
      }
    }
  }
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow hidden
    width 100%
    height 0
    padding-bottom 25%
    background: #eee
    .swiper-img
      width :100%
</style>
