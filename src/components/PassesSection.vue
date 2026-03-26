<script setup lang="ts">
import Button from './Button.vue'

const passes = [
  {
    name: 'Pass Or',
    img: new URL('@/assets/coin-gold.png', import.meta.url).href,
    price: '149€',
    perks: ['Accès VIP', 'Espace lounge', 'Meet & Greet', 'Parking inclus'],
  },
  {
    name: 'Pass Argent',
    img: new URL('@/assets/coin-silver.png', import.meta.url).href,
    price: '89€',
    perks: ['Accès scènes principales', 'Espace détente', 'Parking inclus'],
  },
  {
    name: 'Pass Bronze',
    img: new URL('@/assets/coin-bronze.png', import.meta.url).href,
    price: '49€',
    perks: ['Accès scènes principales', 'Ambiance garantie'],
  },
]
</script>

<template>
  <section class="passes">
    <h2>Billeterie</h2>
    <p class="passes-subtitle">Choisissez votre aventure</p>
    <div class="passes-grid">
      <div v-for="pass in passes" :key="pass.name" class="pass-card">
        <img :src="pass.img" :alt="pass.name" class="pass-coin" />
        <h3>{{ pass.name }}</h3>
        <p class="pass-price">{{ pass.price }}</p>
        <ul class="pass-perks">
          <li v-for="perk in pass.perks" :key="perk">{{ perk }}</li>
        </ul>
        <Button label="Réserver" />
      </div>
    </div>
    <div class="mascot-row">
      <img src="@/assets/radis/mascotte_geradis.png" alt="" class="mascot-left" />
      <img src="@/assets/radis/mascotte_patradis_moins-mal_detoure.png" alt="" class="mascot-right" />
    </div>
  </section>
</template>

<style scoped>
.passes {
  background-color: #e5dac5;
  padding: 5rem 2rem 0;
  text-align: center;
  position: relative;
  overflow: hidden;
}

h2 {
  font-size: clamp(2.5rem, 6vw, 4rem);
  font-weight: 900;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  color: #47311e;
  margin-bottom: 0.5rem;
}

.passes-subtitle {
  font-size: 1.1rem;
  font-weight: 600;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: #47311e;
  opacity: 0.6;
  margin-bottom: 3rem;
}

.passes-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  max-width: 960px;
  margin: 0 auto;
}

.pass-card {
  background: #fff8ee;
  border: 3px solid #47311e;
  box-shadow: 6px 6px 0 #47311e;
  border-radius: 4px;
  padding: 2rem 1.5rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.75rem;
  transition: transform 0.2s ease;
}

.pass-card:hover {
  transform: translateY(-4px);
}

.pass-coin {
  width: 100px;
  height: 100px;
  object-fit: contain;
}

h3 {
  font-size: 1.3rem;
  font-weight: 900;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: #47311e;
}

.pass-price {
  font-size: 2rem;
  font-weight: 900;
  color: #47311e;
}

.pass-perks {
  list-style: none;
  padding: 0;
  margin: 0.5rem 0 1rem;
  width: 100%;
  text-align: left;
}

.pass-perks li {
  padding: 0.3rem 0;
  font-size: 0.9rem;
  color: #47311e;
  opacity: 0.8;
  border-bottom: 1px solid rgba(71, 49, 30, 0.15);
}

.pass-perks li::before {
  content: '✦ ';
  opacity: 0.5;
}

.mascot-row {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  margin-top: 4rem;
  pointer-events: none;
}

.mascot-left,
.mascot-right {
  width: min(200px, 25vw);
  height: auto;
}

.mascot-right {
  transform: scaleX(-1);
}

@media (max-width: 700px) {
  .passes-grid {
    grid-template-columns: 1fr;
    max-width: 360px;
  }

  .mascot-row {
    display: none;
  }
}
</style>
