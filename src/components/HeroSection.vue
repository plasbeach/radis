<script setup lang="ts">
import Button from './Button.vue'
</script>

<template>
  <section class="hero">
    <img class="hero-logo" src="@/assets/Le_Radis_Festival_HD_v2_long.png" alt="Le Radis Festival" />
    <p class="hero-tagline">Musique · Nature · Convivialité</p>
    <img class="hero-mascot" src="@/assets/radis/mascotte_geradis.png" alt="" />
    <p class="hero-description">
      Nous avons le plaisir de vous inviter à la 4ème édition du Radis Festival,<br />
      Le vendredi 21 et samedi 22 août 2026 !
    </p>
  </section>
</template>

<style scoped>
.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  min-height: 100vh;
  padding: 8rem 2rem 8rem;
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
  color: var(--color-brown-dark);
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

.hero-description {
  font-size: clamp(1.2rem, 2.5vw, 1.8rem);
  font-weight: 600;
  color: var(--color-brown-dark);
  text-align: center;
  margin-top: 1.5rem;
  opacity: 0.85;
}

.hero-mascot {
  width: min(400px, 55vw);
  height: auto;
  margin-top: 1rem;
  filter: drop-shadow(0 8px 24px rgba(var(--color-brown-dark-rgb), 0.2));
}
</style>
