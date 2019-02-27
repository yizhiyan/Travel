<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <router-link to="/search">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
      </router-link>
    </div>
    <div class="header-right">
      城市
      <span class="iconfont arrow-icon">&#xe64a;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'home-header'
}
</script>

<style scoped lang="stylus">
@import "~styles/varibies.styl"
.header
  display:flex
  background:$bgColor
  height:.86rem;
  line-height:.86rem
  color:#fff
  .header-left
    width:.64rem
    float:left
    .back-icon
      font-size:.4rem
      text-align:center
  .header-input
    flex:1
    background:#fff
    border-radius:.1rem
    margin-top:.12rem
    margin-left:.2rem
    height:.64rem
    line-height:.64rem
    color: #ccc
    padding-left:.2rem
    a
      color: #e4e7ea
  .header-right
    width:1.24rem
    float: right
    text-align:center
    .arrow-icon
      font-size:.18rem
      position relative
      top:-.04rem
</style>
