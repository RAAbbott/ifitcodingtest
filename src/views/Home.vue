<template>
  <div class="mainView">
    <Splash/>
    <Slider/>
    <Workouts/>
    <Equipment/>
  </div>
</template>

<script>
// @ is an alias to /src
import Splash from '../components/SplashImage.vue';
import Slider from '../components/Slider.vue';
import Workouts from '../components/Workouts.vue';
import Equipment from '../components/Equipment.vue';


export default {
  components: {
    Splash,
    Slider,
    Workouts,
    Equipment
  }
};
</script>

<style scoped>

</style>