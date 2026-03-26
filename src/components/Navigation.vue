<script setup lang="ts">
import Button from './Button.vue'
</script>

<template>
  <nav>
    <img src="@/assets/radis/mascotte_geradis.png" alt="Radis Festival" class="nav-logo" />
    <ul>
      <li><Button label="Emplacement" /></li>
      <li><Button label="Programmation" /></li>
      <li><Button label="Billetterie" /></li>
    </ul>
  </nav>
</template>

<style scoped>
nav {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0.75rem 2rem;
  background-color: #e5dac5;
  border-bottom: 3px solid #47311e;
  box-shadow: 0 2px 0 #2e1e11;
}

.nav-logo {
  height: 52px;
  width: auto;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}
</style>
