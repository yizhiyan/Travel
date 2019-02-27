<template>
  <search-template title="热门搜索" :button="buttonInfo">
    <div class="scenery">
      <div><img src="http://img1.qunarzz.com/piao/fusion/1511/da/8c3405b0e7d493f7.png"></div>
      <a href="javascript:;" v-for="it in sceneryList" :key="it">{{it}}</a>
    </div>
    <div class="scenery address">
      <div><img src="http://img1.qunarzz.com/piao/fusion/1511/e8/d46972e07444bbf7.png"></div>
      <a href="javascript:;" v-for="it in addressList" :key="it">{{it}}</a>
    </div>
    <div class="searchRen">
      <div>搜索身边的景点</div>
    </div>
  </search-template>
</template>

<script>
import SearchTemplate from './SearchTemplate.vue'
export default {
  name: 'search-push',
  data () {
    return {
      buttonInfo: {
        text: '换一批',
        icon: '&#xe650;',
        click () {
          console.log(this)
        }
      },
      addressList: [
        '陕西省',
        '西昌市',
        '重庆',
        '自贡',
        '宜宾'
      ],
      sceneryList: [
        '温泉滑雪折上再减',
        '精品小团立减15',
        '一日游领卷减15',
        '峨眉山',
        '都江堰'
      ]
    }
  },
  components: {
    SearchTemplate
  }
}
</script>

<style scoped lang="scss">
  .scenery{
    height: 1.8rem;
    border-bottom: 1px solid #dce5e7;
    overflow: hidden;
    div{
      width: .76rem;
      text-align: center;
      height: 100%;
      float: left;
      position: relative;
      &::after{
        display: block;
        position: absolute;
        top: 14%;
        right: 0;
        height:68%;
        border-right: 1px solid #dce5e7;
        content: '';
      }
      img{
        width: .3rem;
        height: .3rem;
        position: relative;
        top: 50%;
        margin-top: -.15rem;
      }
    }
    a{
      float: left;
      height: .36rem;
      max-width: 2.89rem;
      line-height: .36rem;
      text-align: center;
      display: block;
      padding-left: .3rem;
      padding-right: .3rem;
      border-right: 1px dashed #c9cccd;
      color: #333;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      margin-top: .25rem;
      margin-bottom: .25rem;
    }
  }
  .address{
    max-height: .9rem;
    a{
      float: left;
      height: .36rem;
      width: 13.6%;
      line-height: .36rem;
      text-align: center;
      display: block;
      border-right: 1px dashed #c9cccd;
      color: #333;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      margin-top: .25rem;
      margin-bottom: .25rem;
    }
  }
  .searchRen{
    padding: .2rem;
    div{
      height: .76rem;
      line-height: .76rem;
      text-align: center;
      font-size: .26rem;
      color: #333;
      border: 1px solid #dde1e3;
      border-radius: 2px;
    }
  }
</style>
