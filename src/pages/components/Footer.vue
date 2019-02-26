<template>
  <div class="footer-container">
    <ul class="footer-links">
      <li v-for="(it,index) in iconList" :key="index" v-if="index<3?true:isShow">
        <div class="icon" :class="it.icon"></div>
        <a href="javascript:;">{{it.title}}</a>
      </li>
      <li class="button" @click="setIsShow()"><i class="iconfont" :class="!isShow?'isShow':''">&#xe631;</i>{{!isShow?'更多':'收起'}}</li>
    </ul>
    <div class="footer-function">
      <a href="javascript:;">登录</a>
      <a href="javascript:;">我的订单</a>
      <a href="javascript:;">最近浏览</a>
      <a href="javascript:;">关于我们</a>
    </div>
    <div class="footer-phone">
      <a href="javascript:;" class="this">触屏版</a>
      <a href="javascript:;">电脑版</a>
    </div>
    <div class="footer-bot">Qunar 京ICP备05021087意见反馈</div>
  </div>
</template>

<script>
export default {
  name: 'home-footer',
  data () {
    return {
      iconList: [
        {
          title: '机票',
          icon: 'icon-1'
        },
        {
          title: '酒店',
          icon: 'icon-2'
        },
        {
          title: '团购',
          icon: 'icon-3'
        },
        {
          title: '景点',
          icon: 'icon-4'
        },
        {
          title: '接送机',
          icon: 'icon-5'
        },
        {
          title: '车车',
          icon: 'icon-6'
        },
        {
          title: '公寓',
          icon: 'icon-7'
        },
        {
          title: '度假',
          icon: 'icon-8'
        },
        {
          title: '飞机',
          icon: 'icon-9'
        },
        {
          title: '火车票',
          icon: 'icon-10'
        },
        {
          title: '攻略',
          icon: 'icon-11'
        },
        {
          title: '旅游',
          icon: 'icon-12'
        }
      ],
      isShow: false
    }
  },
  methods: {
    setIsShow () {
      this.isShow = !this.isShow
      console.log('111')
    }
  }
}
</script>

<style scoped lang="scss">
.footer-links{
  padding:0 .4rem;
  text-align: center;
  &::after{
    content: '';
    clear: both;
    display: block;
  }
  li{
    display: inline-block;
    width: 1.50rem;
    line-height: .3rem;
    height: .3rem;
    margin: .18rem 0;
    font-size: 12px;
    &::after{
      display: block;
      content: '';
      clear: both;
    }
    .icon{
      float: left;
      width: 22px;
      height: 22px;
      background: url(/static/image/nav_7.png) 0 0 no-repeat;
      background-position-x: 0px;
      background-position-y: 0px;
      background-size: 175px 50px;
      position: relative;
      top: -.02rem;
    }
    @for $i from 0 to 12{
      @if $i<7 {
        .icon-#{$i+1}{
          background: url(/static/image/nav_7.png) (($i*50+1+$i/2)/100*-1)+rem 0rem no-repeat;
          background-size: 175px 50px;
        }
      }
      @else{
        .icon-#{$i+1}{
          $p:$i - 7;
          background: url(/static/image/nav_7.png) (($p*50+1+$p/2)/100*-1)+rem (0.54*-1)+rem no-repeat;
          background-size: 175px 50px;
        }
      }
    }
    a{
      color: #9e9e9e;
      margin: .06rem 0 0 .10rem;
      border-bottom: 1px solid #acacac;
      float: left;
    }
  }
}
.button{
  float: right;
  position: relative;
  color: #9e9e9e;
  left: -.26rem;
  padding-top: .1rem;
  height: .24rem;
  i{
    font-size: .20rem;
    position: relative;
    top: -.04rem;
    left: -.08rem;
    display: inline-block;
    &.isShow{
      transform: scaleY(-1);
    }
  }
  &::before{
    position: absolute;
    top: .1rem;
    left: -.02rem;
    width: .02rem;
    height: .24rem;
    background: #acacac;
    content: '';
  }
}
.footer-function{
  border-bottom: 1px solid #e0e0e0;
  a{
    padding-left: .3rem;
    display: inline-block;
    line-height: .8rem;
    color: #25a4bb;
  }
}
.footer-phone{
  text-align: center;
  padding: .2rem 0;
  a{
    margin: 0 .4rem;
    &.this{
      color: black;
    }
  }
}
.footer-bot{
  color: #9e9e9e;
  text-align: center;
  font-size: 14px;
  padding-bottom: .2rem;
}
</style>
