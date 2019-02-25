<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-popular></home-popular>
    <home-guess></home-guess>
    <home-weekend></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icon'
import HomePopular from './components/Popular'
import HomeGuess from './components/Guess'
import HomeWeekend from './components/weekend'

export default {
  name: 'home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomePopular,
    HomeGuess,
    HomeWeekend
  }
}
</script>

<style>
</style>
