<template>
  <search-template title="搜索历史" :button="buttonInfo" v-if="diaryList&&diaryList.length>0">
    <div class="content">
      <a href="javascript:;" v-for="(it,index) in diaryList" :key="index">{{it}}</a>
    </div>
  </search-template>
</template>

<script>
import SearchTemplate from './SearchTemplate.vue'
export default {
  name: 'search-diary',
  data () {
    return {
      buttonInfo: {
        text: '清除',
        icon: '&#xe614;',
        click () {
          this.$parent.$parent.removeCookieAll()
        }
      }
    }
  },
  props: {
    diaryList: Array
  },
  components: {
    SearchTemplate
  }
}
</script>

<style scoped lang="scss">
.content{
  height: 1.24rem;
  padding: .3rem 0 0 0;
  box-sizing: border-box;
  overflow-x: scroll;
  overflow-y: hidden;
  white-space: nowrap;
  &::after{
    display: block;
    content:'';
    clear: both;
  }
  a{
    display: inline-block;
    max-width: 2.89rem;
    height: .6rem;
    font-size: .26rem;
    color: #333;
    background-color: #fff;
    line-height: .6rem;
    padding: 0 .15rem;
    text-align: center;
    margin-left: .2rem;
    border: 1px solid #c9cccd;
    border-radius: 3px;
    white-space: nowrap;
    text-overflow: ellipsis;
    overflow: hidden;
  }
}
</style>
