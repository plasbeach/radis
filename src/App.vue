<script setup lang="ts">
import Navigation from '@/components/Navigation.vue'
import HeroSection from '@/components/HeroSection.vue'
import SoilDivider from '@/components/SoilDivider.vue'
import AboutSection from '@/components/AboutSection.vue'
import CrowdSection from '@/components/CrowdSection.vue'
import PassesSection from '@/components/PassesSection.vue'
</script>

<template>
  <Navigation />
  <main>
    <HeroSection />
    <SoilDivider />
    <AboutSection />
    <SoilDivider :flipped="true" />
    <CrowdSection />
    <SoilDivider />
    <PassesSection />
  </main>
</template>

<style scoped>
main {
  overflow: hidden;
}
</style>
