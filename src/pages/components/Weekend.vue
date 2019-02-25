<template>
  <div class="weekend-container">
    <div class="weekend-title">周末去哪儿</div>
    <ul class="weekend-list">
      <li v-for="(it,index) in dataList" :key="index">
        <img :src="it.img" alt="">
        <div class="weekend-info">
          <h3>{{it.title}}</h3>
          <div class="weekend-introduce">{{it.info}}</div>
        </div>
      </li>
    </ul>
    <div class="tips">
      <i class="iconfont">&#xe661;</i>
      <strong>票面价</strong>是指通过景区指定窗口售卖的纸质门票上标注的价格
    </div>
  </div>
</template>

<script>
export default {
  name: 'home-weekend',
  data () {
    return {
      dataList: [
        {
          img: 'http://img1.qunarzz.com/sight/source/1505/98/47e8d7bdbed162.jpg_r_640x214_f6059302.jpg',
          title: '有温泉就是任性',
          info: '繁忙的一周结束，拖着疲惫的身体赶紧来泡个养生温泉吧，解除你的疲劳\n'
        },
        {
          img: 'http://img1.qunarzz.com/sight/source/1505/a2/78e4dbcfd45a6d.jpg_r_640x214_7a62b06a.jpg',
          title: '成都必打卡',
          info: '成都的标志，也是现代人对老成都的记忆'
        },
        {
          img: 'http://img1.qunarzz.com/sight/source/1811/65/7322301be0a92c.jpg_r_640x214_a3485c55.jpg',
          title: '摩崖石刻造像',
          info: '诸事不顺，来抱佛脚，中国最壮观的大佛大盘点~来一场真正的“佛”系之旅，乐山大佛是首选\n'
        },
        {
          img: 'http://img1.qunarzz.com/sight/source/1601/ee/87a4630fdc1485.jpg_r_640x214_99dc3e82.jpg',
          title: '冰瀑节，相约美丽中国',
          info: '康巴大地上的连绵雪山和不羁的江河，肥沃的田园和诗意的牧场，让这篇神秘之地幸福永恒\n'
        },
        {
          img: 'http://img1.qunarzz.com/sight/source/1505/63/0ffcb5c329a19c.jpg_r_640x214_93fd1e5a.jpg',
          title: '成都文艺范儿',
          info: '《成都》唱火了这里，其实这儿不只有酒馆，还有很多文艺爆棚的地方'
        }
      ]
    }
  }
}
</script>

<style scoped lang="stylus">
.weekend-title
  height .8rem
  line-height .8rem
  padding-left .2rem
  color: #212121;
.weekend-list li
  background white
  margin-bottom .1rem
  img
    width 100%
  .weekend-info
    padding .2rem
    h3
      overflow: hidden;
      padding-right: 1.4rem;
      color: #212121;
      font-size: .28rem;
      line-height: .48rem;
      white-space: nowrap;
      text-overflow: ellipsis;
    .weekend-introduce
      overflow: hidden;
      padding-right: 1.4rem;
      color: #616161;
      font-size: .24rem;
      line-height: .42rem;
      white-space: nowrap;
      text-overflow: ellipsis;
.tips
  display block
  background white
  font-size: .24rem;
  line-height: .60rem;
  color: #616161;
  padding-left .2rem
  .iconfont
    position relative
    font-size .24rem
</style>
