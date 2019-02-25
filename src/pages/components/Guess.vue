<template>
  <div class="guess-container">
    <div class="guess-titles"><i class="iconfont">&#xe63b;</i><span>猜猜你喜欢</span></div>
    <ul class="guess-list">
      <li v-for="(it,index) in dataList" :key="index">
        <div class="guess-icons">{{it.info}}</div>
        <div class="guess-img">
          <img style="" :src="it.img" alt="">
        </div>
        <div class="guess-right">
          <div class="guess-title">{{it.title}}</div>
          <span class="guess-ic">
            <strong class="iconfont">&#xe60d;&#xe60d;&#xe60d;&#xe60d;&#xe60d;&#xe60d;</strong>
            <span>{{it.comment}}条评论</span>
          </span>
          <div class="guess-info">
            <span class="guess-money">￥<em>{{it.money}}</em></span>起
            <span class="guess-address">{{it.address}}</span>
          </div>
          <div class="guess-tips" v-if="it.tips">
            <span>{{it.tips}}</span>
          </div>
        </div>
      </li>
    </ul>
    <a href="javascript:;" class="guess-whole">查看所有产品</a>
  </div>
</template>

<script>
export default {
  name: 'home-guess',
  data () {
    return {
      dataList: [
        {
          title: '天府花溪谷山地户外运动体验公园',
          money: 29.9,
          address: '大邑县',
          comment: 1450,
          img: 'http://img1.qunarzz.com/sight/p0/1707/f6/f60edcaa8934d4fda3.img.jpg_200x200_37d0eedd.jpg',
          grade: 6,
          info: '随买随用'
        },
        {
          title: '石象湖',
          money: 40,
          address: '蒲江县',
          comment: 3422,
          img: 'http://img1.qunarzz.com/sight/p0/1809/1f/1f39774291457a42a3.img.jpg_200x200_e2d8001d.jpg',
          grade: 6,
          info: '随买随用'
        },
        {
          title: '成都海昌极地海洋公园',
          money: 88,
          address: '双流县',
          comment: 31534,
          img: 'http://img1.qunarzz.com/sight/p0/1612/1d/1d9a740c1f9e0efaa3.img.jpg_200x200_63285bd9.jpg',
          grade: 6,
          info: '随买随用',
          tips: '蠢萌企鹅陪你嗨翻这个秋'
        },
        {
          title: '西岭雪山',
          money: 89,
          address: '大邑县',
          comment: 11465,
          img: 'http://img1.qunarzz.com/sight/p0/1508/53/53c486532f848d71.img.jpg_200x200_c4be246c.jpg',
          grade: 6,
          info: '随买随用'
        },
        {
          title: '成都熊猫基地',
          money: 27,
          address: '成华区',
          comment: 120688,
          img: 'http://img1.qunarzz.com/sight/p0/201309/24/977fea7b3c5cd758c8d65eac.jpg_200x200_697c3b3f.jpg',
          grade: 6,
          info: '随买随用',
          tips: '看！熊猫宝宝在想你招手呢'
        },
        {
          title: '西岭雪山滑雪场',
          money: 89,
          address: '西岭雪山',
          comment: 3455,
          img: 'http://img1.qunarzz.com/sight/p0/1505/90/90c1bc45fe24299a.water.jpg_200x200_ef275228.jpg',
          grade: 6,
          info: '随买随用',
          tips: '中国大型高山滑草场，多雪静风乐趣无穷'
        },
        {
          title: '青城道温泉',
          money: 168,
          address: '都江堰市',
          comment: 2134,
          img: 'http://img1.qunarzz.com/sight/p0/201301/16/ae96ce4058bd5cf093835fbb.jpg_200x200_e4cb9743.jpg',
          grade: 6,
          info: '随买随用'
        },
        {
          title: '天府花溪谷山地户外运动体验公园',
          money: 29.9,
          address: '大邑县',
          comment: 1450,
          img: 'http://img1.qunarzz.com/sight/p0/1707/f6/f60edcaa8934d4fda3.img.jpg_200x200_37d0eedd.jpg',
          grade: 6,
          info: '随买随用'
        },
        {
          title: '石象湖',
          money: 40,
          address: '蒲江县',
          comment: 3422,
          img: 'http://img1.qunarzz.com/sight/p0/1809/1f/1f39774291457a42a3.img.jpg_200x200_e2d8001d.jpg',
          grade: 6,
          info: '随买随用'
        },
        {
          title: '成都海昌极地海洋公园',
          money: 88,
          address: '双流县',
          comment: 31534,
          img: 'http://img1.qunarzz.com/sight/p0/1612/1d/1d9a740c1f9e0efaa3.img.jpg_200x200_63285bd9.jpg',
          grade: 6,
          info: '随买随用',
          tips: '蠢萌企鹅陪你嗨翻这个秋'
        },
        {
          title: '西岭雪山',
          money: 89,
          address: '大邑县',
          comment: 11465,
          img: 'http://img1.qunarzz.com/sight/p0/1508/53/53c486532f848d71.img.jpg_200x200_c4be246c.jpg',
          grade: 6,
          info: '随买随用'
        },
        {
          title: '成都熊猫基地',
          money: 27,
          address: '成华区',
          comment: 120688,
          img: 'http://img1.qunarzz.com/sight/p0/201309/24/977fea7b3c5cd758c8d65eac.jpg_200x200_697c3b3f.jpg',
          grade: 6,
          info: '随买随用',
          tips: '看！熊猫宝宝在想你招手呢'
        },
        {
          title: '西岭雪山滑雪场',
          money: 89,
          address: '西岭雪山',
          comment: 3455,
          img: 'http://img1.qunarzz.com/sight/p0/1505/90/90c1bc45fe24299a.water.jpg_200x200_ef275228.jpg',
          grade: 6,
          info: '随买随用',
          tips: '中国大型高山滑草场，多雪静风乐趣无穷'
        },
        {
          title: '青城道温泉',
          money: 168,
          address: '都江堰市',
          comment: 2134,
          img: 'http://img1.qunarzz.com/sight/p0/201301/16/ae96ce4058bd5cf093835fbb.jpg_200x200_e4cb9743.jpg',
          grade: 6,
          info: '随买随用'
        }
      ]
    }
  }
}
</script>

<style scoped lang="stylus">
@import '~styles/mixins.styl'
@import '~styles/varibies.styl'
.guess-container
  background white
  margin-top .2rem
.guess-titles
  position: relative;
  padding: .24rem .2rem .26rem;
  i
    color #ff5163
    font-size: .34rem;
  span
    display: inline-block;
    margin-left: .08rem;
    height: .44rem;
    color: #212121;
    font-size: .32rem;
    line-height: .44rem;
.guess-list li
  position relative
  padding .2rem
  border-bottom:.02rem solid $borderColor
.guess-list li::after
  display block
  content: ''
  clear: both
.guess-icons
  position: absolute;
  top: .2rem;
  left: .2rem;
  width: 1.02rem;
  height: .38rem;
  background-size: 100%;
  color: #fff;
  font-size: .2rem;
  line-height: .38rem;
  text-indent: .04rem;
  background:url('https://img1.qunarzz.com/piao/fusion/1802/20/2ba6d10b17972e02.png')
  border-radius 0 0 .2rem 0
.guess-img,.guess-img img
  width 2rem
  height 2rem
  float: left
.guess-right
  padding-left 2.22rem
.guess-title
  margin-top: .26rem;
  height: .44rem;
  color: #212121;
  font-size: .32rem;
  line-height: .44rem;
  width 100%
  ellipse()
.guess-ic
  display block
  margin-top .18rem
  strong.iconfont
    font-size .22rem
    letter-spacing:.02rem;
    color: #ffb436
  span
    color: #616161;
    font-size: .24rem;
    line-height: .34rem;
    vertical-align: text-bottom;
    position relative
    top:.02rem
    left .1rem
.guess-info
  position: relative;
  margin-top: .22rem;
  color: #616161;
  font-size: .24rem;
  line-height: .4rem;
.guess-money
  color: #ff8300;
  em
    font-size: .4rem;
.guess-address
  float right
.guess-tips
  display: inline-block;
  margin-top: .48rem;
  margin-right: .24rem;
  background: #fff9f9;
  padding: .04rem .1rem;
  color: #f55;
  font-size: .24rem;
  line-height: .34rem;
.guess-whole
  display block
  height .4rem
  line-height .4rem
  padding .2rem 0
  text-align center
  color: #00afc7
  background white
  font-size .28rem
</style>
