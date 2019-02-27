<template>
  <div class="header-container">
    <div class="header-return iconfont" @click="goReturn()">&#xe624;</div>
    <input class="search-input" v-model="SearchContext" type="text" placeholder="输入城市或景点">
    <div class="header-button-search" @click="Search()">搜索</div>
  </div>
</template>

<script>
export default {
  name: 'search-header',
  data () {
    return {
      SearchContext: ''
    }
  },
  methods: {
    goReturn () {
      this.$router.go(-1)
    },
    Search () {
      this.$emit('addCookie', this.SearchContext)
    }
  }
}
</script>

<style scoped lang="scss">
.header-container{
  height: .88rem;
  line-height: .88rem;
  background: white;
  width: 100%;
  border-bottom: 1px solid #e0e0e0;

  display: flex;
  .header-return{
    width: .80rem;
    text-align: center;
    font-weight: bold;
    display: inline-block;
    float: left;
  }
  .search-input{
    display: inline-block;
    height: .4rem;
    line-height: .4rem;
    padding: .1rem .16rem;
    background: #f2f2f2;
    border: 0;
    font-family: "Microsoft Yahei",Arial;
    font-size: .28rem;
    border-radius: .26rem;
    text-align: center;
    flex: 1;
    margin-top: .14rem;
  }
  .header-button-search{
    float: right;
    width: 1rem;
    text-align: center;
  }
}
</style>
