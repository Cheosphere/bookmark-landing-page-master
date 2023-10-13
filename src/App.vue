<script setup>
import FeaturesSection from './components/FeaturesSection.vue';
import HeaderSection from './components/HeaderSection.vue';
import HeroSection from './components/HeroSection.vue';
import DownloadSection from './components/DownloadSection.vue';
import FaqSection from './components/FaqSection.vue'
import NewsletterSection from './components/NewsletterSection.vue';
import FooterSection from './components/FooterSection.vue'
</script>

<template>
  <div class="wrapper">
    <HeaderSection />
    <main class="container">
      <HeroSection />
      <FeaturesSection />
      <DownloadSection />
      <FaqSection />
    </main>
    <NewsletterSection />
    <FooterSection />
  </div>
</template>

<style scoped>
.wrapper {
  width: 100%;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

.container {
  width: 100%;
  max-width: 1440px;
  height: fit-content;
  padding: 0 10.313rem;
  transition: .3s;
}

/* MEDIA QUERY */
@media screen and (max-width: 1380px) {
  .container {
    padding: 0 4rem;
  }

}

@media screen and (max-width: 1240px) {
  .container {
    padding: 0 3rem;
  }
}

@media screen and (max-width: 768px) {
  .container {
    padding: 0 2rem;
  }
}

@media screen and (max-width: 440px) {
  .container {
    padding: 0 1.2rem;
  }
}
</style>
