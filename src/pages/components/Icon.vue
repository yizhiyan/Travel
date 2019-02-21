<template>
  <div class="icons">
    <swiper :options="swiperOption"  autoplay="false">
      <swiper-slide v-for="item in pages" :key="item.title">
        <div v-for="(it,index) in item" :key="index" class="icon">
          <div class="icon-img">
            <img class="icon-img-content" :src="it.icon" :alt="it.title">
          </div>
          <p class="icon-desc">{{it.title}}</p>
        </div>
      </swiper-slide>
    </swiper>
    <div class="icon-swiper-pagination"  slot="pagination"></div>
    <div class="address">
      <div><i class="iconfont">&#xe647;</i>定位失败</div>
      <div><i class="iconfont">&#xe76c;</i>必游榜单</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'home-icons',
  data () {
    return {
      dataList: [{
        icon: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        title: '景点门票'
      },
      {
        icon: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
        title: '一日游'
      },
      {
        icon: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
        title: '成都必游'
      },
      {
        icon: 'http://img1.qunarzz.com/piao/fusion/1803/e3/67df61427c8e1302.png',
        title: '川剧变脸'
      },
      {
        icon: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20191/de711920c71e38287d9f95f7910aa1aa.png',
        title: '精品小团'
      },
      {
        icon: 'http://img1.qunarzz.com/piao/fusion/1803/fc/b10a6b2e4f0fe102.png',
        title: '滑雪'
      },
      {
        icon: 'http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png',
        title: '泡温泉'
      },
      {
        icon: 'http://img1.qunarzz.com/piao/fusion/1803/54/35899492b1302802.png',
        title: '成都熊猫基地'
      },
      {
        icon: 'http://img1.qunarzz.com/piao/fusion/1803/b1/528a9e80403b8c02.png',
        title: '自贡灯会'
      },
      {
        icon: 'http://img1.qunarzz.com/piao/fusion/1803/87/20656da0ac042002.png',
        title: '西岭雪山'
      }],
      swiperOption: {
        pagination: '.icon-swiper-pagination',
        loop: true,
        autoplay: false
      }
    }
  },
  computed: {
    pages () {
      let pages = []
      this.dataList.forEach((item, index) => {
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

<style scoped lang="stylus">
@import '~styles/varibies.styl'
@import '~styles/mixins.styl'
.icons
  overflow hidden
  background white
  >>> .swiper-container
    height :0
    padding-bottom 50%
.icon
  float: left
  width 25%
  padding-bottom 25%
  overflow hidden
  position relative
  box-sizing border-box
  height 0
  .icon-img
    position:absolute
    top:0
    left:0
    right:0
    bottom .44rem
    padding .1rem
    .icon-img-content
      height 100%
      display block
      margin 0 auto
  .icon-desc
    position absolute
    left 0
    right:0
    bottom:0
    height .44rem
    line-height .44rem
    color: $darkTextColor
    text-align center
    font-size .28rem
    ellipse()
.icon-swiper-pagination
  position static
  text-align center
  height .46rem
  line-height .40rem
  >>> .swiper-pagination-bullet
    display inline-block
    margin-right 5px
    width 6px
    height 6px
  >>> .swiper-pagination-bullet-active
    background:rgba(0,175,190,.8)
.address
  height .98rem
  div
    box-sizing border-box
    float left
    width 50%
    line-height .98rem
    text-align center
    border-top:1px solid $borderColor
    border-right 1px solid $borderColor
    font-size .28rem
    i
      margin-right 4px
  div:last-of-type
    border-right none
</style>
