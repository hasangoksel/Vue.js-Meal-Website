<template>
  <navbar></navbar>
  <app-header></app-header>
  <best-food></best-food>
  <the-restaurant></the-restaurant>
  <chefs></chefs>
  <our-menu></our-menu>
  <other-services></other-services>
  <reservation></reservation>
</template>
<script>
import Navbar from './components/Navbar.vue'
import AppHeader from './components/Header.vue';
import BestFood from './components/Best-Food.vue';
import TheRestaurant from './components/The-Restaurant.vue';
import Chefs from './components/Meet-The-Chefs.vue';
import Menu from './components/Our-Menu.vue';
import OtherServices from './components/Other-Services.vue';
import Reservation from './components/Reservation.vue';
export default {
  components: {
    'navbar': Navbar,
    'app-header': AppHeader,
    'best-food': BestFood,
    'the-restaurant': TheRestaurant,
    'chefs': Chefs,
    'our-menu': Menu,
    'other-services': OtherServices,
    'reservation': Reservation
  }
}
</script>
<style scoped></style>
