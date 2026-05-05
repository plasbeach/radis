<template>
  <div class="soil-divider" :class="{ flipped }">
    <div class="mascots">
      <img
        src="@/assets/radis/mascotte_patradis_moins-mal_detoure.png"
        alt="Patradis"
        class="mascot"
        :class="{ risen: risenLeft }"
        @click="risenLeft = !risenLeft"
      />
      <img
        src="@/assets/radis/mascotte_geradis.png"
        alt="Geradis"
        class="mascot"
        :class="{ risen: risenRight }"
        @click="risenRight = !risenRight"
      />
    </div>
    <img src="@/assets/soil.png" alt="" class="soil-img" />
  </div>
  <footer>
    <div>
      <p>Chemin du Vernex</p>
      <p>1721 Cournillens</p>
    </div>
    <div>
      <p>info@radisfestival.ch</p>
      <p>+41 79 674 02 52</p>
    </div>
    <div>
      <a href="https://www.instagram.com/radis.festival/" target="_blank" rel="noopener" class="insta-link">
        <svg xmlns="http://www.w3.org/2000/svg" width="42" height="42" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
          <rect x="2" y="2" width="20" height="20" rx="5" ry="5"/>
          <circle cx="12" cy="12" r="4"/>
          <circle cx="17.5" cy="6.5" r="1" fill="currentColor" stroke="none"/>
        </svg>
      </a>
    </div>
  </footer>
</template>

<script setup lang="ts">
import { ref } from 'vue'
defineProps<{ flipped?: boolean }>()

const risenLeft = ref(false)
const risenRight = ref(false)
</script>

<style scoped>
.soil-divider {
  width: 100%;
  line-height: 0;
  margin-top: 4rem;
  margin-bottom: 0;
  position: relative;
  padding-top: 100px;
}

.soil-img {
  position: relative;
  z-index: 2;
  width: 100%;
  height: 15rem;
  display: block;
  object-fit: cover;
  object-position: top;
  pointer-events: none;
}

.soil-divider.flipped {
  transform: scaleY(-1);
  margin-bottom: 0;
  margin-top: -2px;
}

.mascots {
  position: absolute;
  top: 160px;
  left: 0;
  right: 0;
  display: flex;
  justify-content: center;
  gap: 6rem;
  z-index: 1;
  pointer-events: none;
}

.mascot {
  height: 160px;
  width: auto;
  display: block;
  transform: translateY(-50%);
  transition: transform 0.4s steps(17);
  cursor: pointer;
  pointer-events: auto;
}

.mascot.risen {
  transform: translateY(calc(-50% - 85px));
}

.insta-link {
  color: inherit;
  display: inline-block;
  transition: opacity 0.2s;
}

.insta-link:hover {
  opacity: 0.7;
}

footer {
  position: relative;
  z-index: 200;
  margin: -15rem clamp(2rem, 10vw, 12rem) 0;
  color: var(--color-beige);
  padding: 5rem 0 2rem;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  font-size: clamp(0.7rem, 1.8vw, 1rem);
  div {
    text-align: center;
  }
}

.insta-link svg {
  width: clamp(24px, 4vw, 42px);
  height: clamp(24px, 4vw, 42px);
}
</style>