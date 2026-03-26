<template>
  <div class="soil-divider" :class="{ flipped }">
    <img src="@/assets/soil.png" alt="" />
  </div>
</template>

<script setup lang="ts">
defineProps<{ flipped?: boolean }>()
</script>

<style scoped>
.soil-divider {
  width: 100%;
  overflow: hidden;
  line-height: 0;
  margin-bottom: -2px;
}

.soil-divider img {
  width: 100%;
  height: auto;
  display: block;
  object-fit: cover;
  max-height: 200px;
  object-position: top;
}

.soil-divider.flipped {
  transform: scaleY(-1);
  margin-bottom: 0;
  margin-top: -2px;
}
</style>