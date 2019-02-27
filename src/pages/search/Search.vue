<template>
  <div class="search-container">
    <search-header @addCookie="addCookie" :diaryList="diaryList"></search-header>
    <search-diary :diaryList="diaryList"></search-diary>
    <search-push></search-push>
  </div>
</template>

<script>
import searchHeader from './Header.vue'
import searchDiary from './Diary.vue'
import searchPush from './Push.vue'
export default {
  name: 'search',
  data () {
    return {
      diaryList: []
    }
  },
  created () {
    let val = JSON.parse(this.$cookies.get('diaryList'))
    if (val) {
      this.diaryList = val
    }
  },
  components: {
    searchHeader,
    searchDiary,
    searchPush
  },
  methods: {
    addCookie (text) {
      this.diaryList.push(text)
      if (this.$cookies.isKey('diaryList')) {
        this.$cookies.remove('diaryList')
      }
      this.$cookies.set('diaryList', JSON.stringify(this.diaryList), 2000)
    },
    removeCookieAll () {
      if (this.$cookies.isKey('diaryList')) {
        this.$cookies.remove('diaryList')
        this.diaryList = []
      }
    }
  }
}
</script>

<style scoped lang="scss">
.search-container{
  box-shadow: 0 0 .06rem #c7ced4;
}
</style>
