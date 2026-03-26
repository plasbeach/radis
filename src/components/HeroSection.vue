<script setup lang="ts">
import Button from './Button.vue'
</script>

<template>
  <section class="hero">
    <img class="hero-logo" src="@/assets/logo_trop_swag_radis_inline.png" alt="Le Radis Festival" />
    <p class="hero-tagline">Musique · Nature · Convivialité</p>
    <div class="hero-actions">
      <Button label="Billetterie" />
      <Button label="Programme" />
    </div>
    <img class="hero-mascot" src="@/assets/radis/mascotte_patradis_moins-mal_detoure.png" alt="" />
  </section>
</template>

<style scoped>
.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  padding: 6rem 2rem 0;
  position: relative;
  overflow: hidden;
}

.hero-logo {
  width: min(820px, 90vw);
  height: auto;
}

.hero-tagline {
  font-size: clamp(1rem, 2.5vw, 1.5rem);
  font-weight: 700;
  letter-spacing: 0.3em;
  text-transform: uppercase;
  color: #47311e;
  margin: 1.5rem 0 2.5rem;
  opacity: 0.8;
}

.hero-actions {
  display: flex;
  gap: 1.5rem;
  flex-wrap: wrap;
  justify-content: center;
  margin-bottom: 4rem;
}

.hero-mascot {
  width: min(320px, 55vw);
  height: auto;
  margin-top: auto;
  transform: scaleX(-1);
  filter: drop-shadow(0 8px 24px rgba(71, 49, 30, 0.2));
}
</style>