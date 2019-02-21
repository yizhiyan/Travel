<template>
  <div class="wrapper">
    <swiper :options="swiperOption" ref="mySwiper" >
      <!-- slides -->
      <swiper-slide>
        <img src="http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20191/3921acb51460dc6fa9e3c7464fac5cbb.jpg_750x200_d992573a.jpg" alt="">
      </swiper-slide>
      <swiper-slide>
        <img src="http://img1.qunarzz.com/piao/fusion/1812/d6/daa880b254940402.jpg_750x200_b114308a.jpg" alt="">
      </swiper-slide>
      <swiper-slide>
        <img src="http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20191/a211765c0bb579b18c6e7d6d75997a48.jpg_750x200_b6921fa6.jpg" alt="">
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'home-swiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        scrollbarHide: true,
        autoplay: 2000
      }
    }
  }
}
</script>

<style scoped lang="stylus">
.wrapper
  width:100%;
  height:0;
  overflow:hidden;
  padding-bottom:26.5%
  >>> .swiper-pagination-bullet-active
    background #fff
  img
    width:100%;
</style>
