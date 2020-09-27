<template>
  <v-app>
    <MainNavigation/>
    <CarouselSection/>
    <NewsSection/>
    <GallerySection/>
    <FooterSection/>       
  </v-app>
</template>

<script>
//import HelloWorld from './components/HelloWorld';
import MainNavigation from './components/MainNavigation';
import CarouselSection from './components/CarouselSection';
import NewsSection from './components/NewsSection';
import GallerySection from './components/GallerySection';
import FooterSection from './components/FooterSection';

export default {
  name: 'App',

  components: {    
    MainNavigation,
    CarouselSection,
    NewsSection,
    GallerySection,
    FooterSection,
  },

  data: () => ({
    //
  }),
};
</script>

<style lang="stylus" scoped>

</style>
