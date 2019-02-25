<template>
  <div class="popular-container">
    <div class="popular-titles">
      <i class="iconfont">&#xe6a0;</i>
      <span class="popular-title">本周热门榜单</span>
      <span class="popular-all iconfont">全部榜单&#xe600;</span>
    </div>
    <ul class="popular-list">
      <li v-for="(it,index) in dataList" :key="index">
        <div class="popular-ranking" v-if="it.ranking">
          <img :src="ranking[it.ranking-1]" alt="">
        </div>
        <div class="img-continer">
          <img :src="it.icon" alt="">
        </div>
        <div class="pro-title">{{it.title}}</div>
        <div class="pro-money"><span class="prom">￥<em>{{it.money}}</em></span>起</div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'hade-popular',
  data () {
    return {
      ranking: [
        'http://img1.qunarzz.com/piao/fusion/1710/ab/159673b63e6ca702.png',
        'http://img1.qunarzz.com/piao/fusion/1710/2d/36d0c4adaebbbc02.png',
        'http://img1.qunarzz.com/piao/fusion/1710/67/edc47ffef9e96b02.png'
      ],
      dataList: [
        {
          title: '成都熊猫基地',
          money: 27,
          ranking: 1,
          icon: 'http://img1.qunarzz.com/sight/p0/201309/24/977fea7b3c5cd758c8d65eac.jpg_250x250_145eeeb5.jpg'
        },
        {
          title: '都江堰',
          money: 13,
          ranking: 2,
          icon: 'http://img1.qunarzz.com/sight/p0/201407/03/a584374ee80b738e2600d6bcaf1299e3.jpg_250x250_986e4594.jpg'
        },
        {
          title: '国色天乡·陆地乐园',
          money: 35,
          ranking: 3,
          icon: 'http://img1.qunarzz.com/sight/p0/1704/a5/a59677101e07d38a3.img.jpg_250x250_f664a359.jpg'
        },
        {
          title: '成都动物园',
          money: 10,
          icon: 'http://img1.qunarzz.com/sight/p0/201307/23/b8db11dca4378903c8d65eac.jpg_250x250_aaa0ef4d.jpg'
        },
        {
          title: '西岭雪山滑雪场',
          money: 89,
          icon: 'http://img1.qunarzz.com/sight/p0/1505/90/90c1bc45fe24299a.water.jpg_250x250_c263e78c.jpg'
        },
        {
          title: '西岭雪山',
          money: 89,
          icon: 'http://img1.qunarzz.com/sight/p0/1508/53/53c486532f848d71.img.jpg_250x250_6c61313b.jpg'
        },
        {
          title: '成都海昌极地海洋公园',
          money: 88,
          icon: 'http://img1.qunarzz.com/sight/p0/1612/1d/1d9a740c1f9e0efaa3.img.jpg_250x250_427ee986.jpg'
        },
        {
          title: '成都杜甫草堂',
          money: 47,
          icon: 'http://img1.qunarzz.com/sight/p64/201211/04/9173ff9f33e97f3193835fbb.jpg_250x250_9b1fc434.jpg'
        },
        {
          title: '成都欢乐谷',
          money: 69,
          icon: 'http://img1.qunarzz.com/sight/p0/1807/ad/ad574bfe6c9e1ceda3.img.png_250x250_d7de3c80.png'
        },
        {
          title: '青城山',
          money: 78,
          icon: 'http://img1.qunarzz.com/sight/p0/1505/b0/b0132e78efa00572.water.jpg_250x250_419e0690.jpg'
        }
      ]
    }
  }
}
</script>

<style scoped lang="stylus">
.popular-container
  margin-top:.2rem
  background white
  .popular-titles
    position: relative;
    padding: .24rem 0 .26rem;
    i.iconfont
      color: #ff8644
      font-size: .4rem;
      position relative
      left .14rem
    .popular-all
      position: absolute;
      top: .36rem;
      right: .32rem;
      color: #616161;
      font-size: .24rem;
      line-height: .28rem;
    .popular-title
      display: inline-block;
      margin-left: .08rem;
      height: .44rem;
      color: #212121;
      font-size: .32rem;
      line-height: .44rem;
.popular-list
  padding: 0 .24rem .18rem;
  overflow-x: scroll;
  white-space: nowrap;
  li
    display inline-block
    width 2rem
    position relative
  li:not(:first-child) {
    margin-left: .12rem;
  }
  .popular-ranking
    position: absolute;
    top: 0;
    left: 0;
    z-index: 1;
    overflow: hidden;
    width: .84rem;
    height: .4rem;
    img
      width 100%
  .img-continer
    height 2rem
    width 2rem
    overflow hidden
    img
      width 2rem
  .pro-title
    text-align center
    margin-top .12rem
    font-size .24rem
  .pro-money
    color: #616161;
    font-size: .24rem;
    line-height: .36rem;
    text-align: center;
    span
      color: #ff8300;
      line-height .48rem
      em
        font-size: .28rem;
</style>
