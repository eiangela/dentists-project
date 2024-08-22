<script setup>
import AppBar from '../components/AppBar.vue'
import HeroBanner from '../components/HeroBanner.vue'
import OurTeam from '../components/OurTeam.vue'
import ContactUs from '../components/ContactUs.vue'
import FooterPage from '../components/FooterPage.vue'
</script>

<template>
  <AppBar />
  <section class="intro-section">
    <HeroBanner />
  </section>

  <section class="why-choose-us pa-10">
    <div>
      <h2 class="text-h4 font-weight-bold text-center mb-5">Why choose Us</h2>
    </div>
    <div class="d-flex justify-md-center pa-0 why-wrapper">
      <p class="text-h6 why-paragraph text-center">
        Nam libero justo laoreet sit amet cursus sit amet. Pellentesque habitant morbi tristique
        senectus et netus. Sed augue lacus viverra vitae congue eu. Nunc mattis enim ut tellus
        elementum sagittis vitae.
      </p>
    </div>
    <div class="text-center mt-5">
      <v-btn variant="flat" class="why-btn font-weight-bold" height="66" min-width="208"
        >Contact Us</v-btn
      >
    </div>
  </section>

  <section class="our-team">
    <OurTeam />
  </section>

  <section class="contact-us">
    <ContactUs />
  </section>

  <footer class="footer-page">
    <FooterPage />
  </footer>
</template>
''
