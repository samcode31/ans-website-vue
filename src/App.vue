<template>
  <v-app>
    <NavigationDrawer v-bind:drawer="drawer"/>
    <MainNavigation v-on:drawer-click="drawerClick" />
    <CarouselSection/>
    <NewsSection/>
    <GallerySection/>
    <FooterSection/>       
  </v-app>
</template>

<script>
import NavigationDrawer from './components/NavigationDrawer.vue'
import MainNavigation from './components/MainNavigation';
import CarouselSection from './components/CarouselSection';
import NewsSection from './components/NewsSection';
import GallerySection from './components/GallerySection';
import FooterSection from './components/FooterSection';

export default {
  name: 'App',

  components: {
    NavigationDrawer,    
    MainNavigation,
    CarouselSection,
    NewsSection,
    GallerySection,
    FooterSection,
  },

  created: function () {
    this.initialize();
  },

  data: () => ({
    drawer: false,
  }),

  methods: {
    initialize () {
      console.log('initializing...');
    },

    drawerClick () {
      console.log('drawer click');
      this.drawer = !this.drawer;
    },
    
  }
};
</script>

<style lang="stylus" scoped>

</style>
