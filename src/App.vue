<template>
<AppHeader />
  <div class="w-full flex">
    <router-view></router-view>
    <!-- <DcHeroes /> -->
    <!-- <Calendar /> -->
  </div>
  
</template>

<script>
import AppHeader from './components/AppHeader';
/* import Calendar from './components/Calendar'; */
/* import DcHeroes from './components/DcHeroes'; */

export default {
  components: {AppHeader, /* Calendar */ /* DcHeroes */},
}
</script>

<style>

</style>