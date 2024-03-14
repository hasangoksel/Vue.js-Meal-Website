<template>
  <navbar></navbar>
  <app-header></app-header>
  <best-food></best-food>
  <the-restaurant></the-restaurant>
  <chefs></chefs>
</template>
<script>
// import bölümü
import Navbar from './components/Navbar.vue'
import AppHeader from './components/Header.vue';
import BestFood from './components/Best-Food.vue';
import TheRestaurant from './components/The-Restaurant.vue';
import Chefs from './components/Meet-The-Chefs.vue'
export default {
  components: {
    'navbar': Navbar,
    'app-header': AppHeader,
    'best-food': BestFood,
    'the-restaurant': TheRestaurant,
    'chefs': Chefs
  }
}
</script>
<style scoped></style>
