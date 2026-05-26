<script setup lang="ts">
import { Splide, SplideSlide } from '@splidejs/vue-splide'
import '@splidejs/vue-splide/css'

import img1 from '@/assets/carrousel/DSC_1801.JPG'
import img2 from '@/assets/carrousel/DSC_1753.JPG'
import img3 from '@/assets/carrousel/DSC_1757.JPG'
import img4 from '@/assets/carrousel/IMG-20250829-WA0004.jpg'
import img5 from '@/assets/carrousel/IMG-20250829-WA0006.jpg'
import img6 from '@/assets/carrousel/IMG-20250829-WA0038.jpg'
import img7 from '@/assets/carrousel/IMG-20250829-WA0174.jpg'
import img8 from '@/assets/carrousel/IMG-20250829-WA0425.jpg'

const images = [img1, img2, img3, img4, img5, img6, img7, img8]

const options = {
  rewind: true,
  autoplay: true,
  interval: 4000,
  pauseOnHover: true,
  arrows: true,
  pagination: true,
}
</script>

<template>
  <h1>
    Quelques photos de l'édition 2025 :
  </h1>
  <Splide :options="options" aria-label="Photo carrousel" id="carrousel">
    <SplideSlide v-for="(img, index) in images" :key="index">
      <img :src="img" :alt="`Photo ${index + 1}`" class="slide-img" decoding="async" />
    </SplideSlide>
  </Splide>
</template>

<style scoped>
#carrousel {
  width: min(90%, 1100px);
  margin: 3rem auto;
  border-radius: 1rem;
  overflow: hidden;
  box-shadow: 0 4px 24px rgba(0, 0, 0, 0.15);
}

.slide-img {
  width: 100%;
  aspect-ratio: 16 / 9;
  object-fit: cover;
  display: block;
}

h1 {
  font-size: 3em;
  margin-top: 5rem;
  text-align: center;
}

@media (max-width: 600px) {
  #carrousel {
    width: 100%;
    margin: 5rem;

  }

  .slide-img {
    aspect-ratio: 4 / 3;
  }
}
</style>