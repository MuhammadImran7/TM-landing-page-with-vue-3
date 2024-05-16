<script setup>
import Navbar from './components/Navbar.vue'
import HeaderTop from './components/HeaderTop.vue'
import BannerSlider from './components/BannerSlider.vue'
import ProductListing from './components/ProductListing.vue'
import AboutSection from './components/AboutSection.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <header>
    <div class="container mx-auto">
      <HeaderTop/>
    </div>
    <Navbar/>
    <BannerSlider></BannerSlider>
  </header>
    <ProductListing></ProductListing>
    <AboutSection></AboutSection>
    <Footer></Footer>
</template>

<style scoped>

</style>
