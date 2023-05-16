<script setup>
import Header from '../components/Header.vue';
import InitialBody from '../components/InitialBody.vue';
import Acting from '../components/Acting.vue';
import OurTeam from '../components/OurTeam.vue';
import About from '../components/About.vue';
import Footer from '../components/Footer.vue'

</script>

<template>
  <div>
    <Header />
    <InitialBody />
    <Acting />
    <OurTeam />
    <About />
    <Footer />
  </div>
</template>

<style scoped>
@media only screen and (max-width: 600px) {
  #about {
    height: 1000px;
  }

  #card-two-team {
    margin-top: 40px;
  }
}
</style>
