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
</style>