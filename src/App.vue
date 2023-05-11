<template>
  <div >
    <!-- <AppBar/>
    <SliderWrapper />
    <PageFooter /> -->
    <HeaderBar/>
    <HeroImage/>
  </div>
  
</template>

<script>

// import AppBar from './components/AppBar/AppBar.vue';
// import SliderWrapper from './components/Slider/SliderWrapper.vue';
// import storelocator from './components/Footer/PageFooter.vue'
import HeaderBar from './components/Header/Header_Bar.vue'
import HeroImage from './components/HeroImage/HeroImage.vue';

export default {
  name: 'App',
  components: {
  //  AppBar,
  //  SliderWrapper,
  //  storelocator,
  HeaderBar,
  HeroImage,
 
  }
}
</script>

<style>

</style>
