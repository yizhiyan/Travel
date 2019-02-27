<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-popular></home-popular>
    <home-guess></home-guess>
    <home-weekend></home-weekend>
    <home-footer></home-footer>
  </div>
</template>

<script>
import HomeHeader from './home/Header'
import HomeSwiper from './home/Swiper'
import HomeIcons from './home/Icon'
import HomePopular from './home/Popular'
import HomeGuess from './home/Guess'
import HomeWeekend from './home/Weekend'
import HomeFooter from './home/Footer'

export default {
  name: 'home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomePopular,
    HomeGuess,
    HomeWeekend,
    HomeFooter
  }
}
</script>

<style>
</style>
