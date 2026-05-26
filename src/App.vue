<script setup lang="ts">
import Navigation from '@/components/Navigation.vue'
import HeroSection from '@/components/HeroSection.vue'
import SoilDivider from '@/components/SoilDivider.vue'
import AboutSection from '@/components/AboutSection.vue'
import CrowdSection from '@/components/CrowdSection.vue'
import PassesSection from '@/components/PassesSection.vue'
import Carrousel from '@/components/Carrousel.vue'
</script>

<template>
  <Navigation />
  <main>
    <HeroSection />
    <AboutSection />
    <CrowdSection />
    <Carrousel />
    <soil-divider />
  </main>
</template>

<style scoped>
</style>
