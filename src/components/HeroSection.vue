<script setup lang="ts">
import Button from './Button.vue'
import { computed } from 'vue'

const isApple = computed(() =>
  /iPad|iPhone|iPod|Macintosh/.test(navigator.userAgent)
)

const calendarHref = computed(() =>
  isApple.value
    ? '/radis-festival-2026.ics'
    : 'https://calendar.google.com/calendar/render?action=TEMPLATE&text=Le+Radis+Festival&dates=20260821%2F20260823&details=4%C3%A8me+%C3%A9dition+du+Radis+Festival&location=Chemin+du+Vernex%2C+1721+Cournillens'
)
</script>

<template>
  <section class="hero">
    <img
      class="hero-logo"
      src="@/assets/Le_Radis_Festival_HD_v2_long.png"
      alt="Le Radis Festival"
    />
    <img class="hero-mascot" src="@/assets/radis/mascotte_geradis.png" alt="" />
    <p class="hero-description">
      Nous avons le plaisir de vous inviter à <br />la 4ème édition du Radis Festival<br />
      <a
        class="hero-date-link"
        :href="calendarHref"
        target="_blank"
        rel="noopener"
      >Le vendredi 21 et samedi 22 août 2026</a> !
    </p>
  </section>
</template>

<style scoped>
.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  min-height: 100dvh;
  padding: 8rem 2rem 4rem;
  position: relative;
  overflow: hidden;
}

.hero-logo {
  width: min(820px, 90vw);
  height: auto;
}

.hero-tagline {
  font-size: clamp(0.6rem, 2.5vw, 1.5rem);
  font-weight: 700;
  letter-spacing: clamp(0.05em, 0.3em, 0.3em);
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
  font-size: clamp(1.4rem, 4vw, 3rem);
  font-weight: 700;
  color: var(--color-brown-dark);
  text-align: center;
  opacity: 0.85;
  line-height: 1.5;
}

.hero-date-link {
  color: inherit;
  text-decoration: underline;
  text-decoration-style: dashed;
  text-underline-offset: 4px;
  transition: opacity 0.2s;
}

.hero-date-link:hover {
  opacity: 0.65;
}

.hero-mascot {
  width: clamp(120px, 40vw, 400px);
  height: auto;
  margin-top: 1rem;
  filter: drop-shadow(0 8px 24px rgba(var(--color-brown-dark-rgb), 0.2));
}

@media (max-width: 899px) {
  .hero {
    padding-top: 120px;
  }
}
</style>
