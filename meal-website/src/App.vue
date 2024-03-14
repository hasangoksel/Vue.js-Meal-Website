<template>
  <navbar></navbar>
  <app-header></app-header>
  <best-food></best-food>
  <the-restaurant></the-restaurant>
  <chefs></chefs>
  <our-menu></our-menu>
</template>
<script>
// import bölümü
import Navbar from './components/Navbar.vue'
import AppHeader from './components/Header.vue';
import BestFood from './components/Best-Food.vue';
import TheRestaurant from './components/The-Restaurant.vue';
import Chefs from './components/Meet-The-Chefs.vue';
import Menu from './components/Our-Menu.vue';
export default {
  components: {
    'navbar'        : Navbar,
    'app-header'    : AppHeader,
    'best-food'     : BestFood,
    'the-restaurant': TheRestaurant,
    'chefs'         : Chefs,
    'our-menu'      : Menu
  }
}
</script>
<style scoped></style>
