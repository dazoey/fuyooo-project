<script>
import NavbarComponent from '../components/header/navbar/NavbarComponent.vue'
import HeroSection from '../components/header/hero/HeroSection.vue'
import FiturSection from '../components/body/FiturSection.vue'
import CaraKerja from '../components/body/CaraKerja.vue'
import DampakSection from '../components/body/DampakSection.vue'
import FooterSection from '../components/footer/FooterSection.vue'

export default {
  name: 'HomeView',
  components: {
    NavbarComponent,
    HeroSection,
    FiturSection,
    CaraKerja,
    DampakSection,
    FooterSection
  }
}
</script>

<template>
  <div>
    <NavbarComponent/>
    <main>
      <HeroSection />
      <FiturSection id="Fitur-section"/>
      <CaraKerja id="CaraKerja-section" class="CaraKerja-section"/>
      <DampakSection />
    </main>
    <FooterSection id="About-section" />
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

body {
  color: #333;
  background-color: #fff;
  overflow-x: hidden;
}

.container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}
</style>
