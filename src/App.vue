<template>
  <div id="app">
    <HeaderComponent />
    <BannerComponent />
    <AboutComponent />
    <ServicesTableComponent />
    <ContactFormComponent />
    <GalleryComponent />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import BannerComponent from './components/BannerComponent.vue';
import AboutComponent from './components/AboutComponent.vue';
import ServicesTableComponent from './components/ServicesTableComponent.vue';
import ContactFormComponent from './components/ContactFormComponent.vue';
import GalleryComponent from './components/GalleryComponent.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    BannerComponent,
    AboutComponent,
    ServicesTableComponent,
    ContactFormComponent,
    GalleryComponent,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


</style>
