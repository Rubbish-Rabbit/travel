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
          imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/2f5f3ea4698c9b7898db7562d89b91ed.jpg_750x200_bd3b4ce9.jpg'
        },{
          id:'0002',
          imgUrl: 'https://imgs.qunarzz.com/piao/fusion/1609/e8/a26190adcdc51c02.jpg_750x200_c4691cbe.jpg'
        },{
          id:'0003',
          imgUrl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/c5e84c198ca6a3e8b7e9946144ebefb5.jpg_750x200_43eebad0.jpg'
        },{
          id:'0004',
          imgUrl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/87a224d0349d94a11e97f31aa1aba4f5.jpg_750x200_1f78af87.jpg'
        },{
          id:'0005',
          imgUrl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20192/31a560a7b8f9c26bc8121e141b25d5a6.png_750x200_2775ea25.png'
        },{
          id:'0006',
          imgUrl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/942d87cc1576c333c77dc1f86af145cd.jpg_750x200_d25bf3eb.jpg'
        },{
          id:'0007',
          imgUrl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/ed5f4115226306e48e6fad106a038afe.jpg_750x200_64df48d6.jpg'
        },{
          id:'0008',
          imgUrl:'https://imgs.qunarzz.com/piao/fusion/1609/e8/a26190adcdc51c02.jpg_750x200_c4691cbe.jpg'
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
