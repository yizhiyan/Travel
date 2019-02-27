<template>
  <div class="temp-container">
    <div class="temp-head">
      <span class="head-title">{{title}}</span>
      <span class="head-button" @click="callback()">
        <i class="iconfont" v-html="button.icon"></i>{{button.text}}
      </span>
    </div>
    <div class="temp-content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'search-template',
  props: {
    title: String,
    button: Object
  },
  methods: {
    callback () {
      if (this._props.button.click) {
        this._props.button.click.call(this)
      }
    }
  }
}
</script>

<style scoped lang="scss">
.temp-head{
  height: .64rem;
  line-height: .64rem;
  background: #f0f5f6;
  padding: 0 .2rem;
  .head-title{
    font-size: .26rem;
    color: #888;
  }
  .head-button{
    float: right;
    font-size: .26rem;
    color: #00afc7;
    .iconfont{
      font-size: .24rem;
      position: relative;
      left: -.08rem;
      top: -.02rem;
    }
  }
}
.temp-content{
  width: 100%;
  overflow-y: hidden;
  background-color: #fff;
  border-top: 1px solid #dce5e7;
  border-bottom: 1px solid #dce5e7;
}
</style>
