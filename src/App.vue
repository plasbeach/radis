<script setup lang="ts">
import Navigation from '@/components/Navigation.vue'
import Title from '@/components/Title.vue'
</script>

<template>
  <div class="body">
    <Navigation />
    <Title />
  </div>
</template>

<style scoped>
.body {
  padding: 2rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
</style>
