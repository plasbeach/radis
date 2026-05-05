<script setup lang="ts">
import Button from './Button.vue'

function scrollTo(id: string) {
  document.getElementById(id)?.scrollIntoView({ behavior: 'smooth' })
}

function openBenevoles() {
  window.open('https://forms.gle/tfquPqMHxp98u4tLA', '_blank')
}
</script>

<template>
  <nav>
    <div class="title">
      <img src="@/assets/radis/mascotte_geradis.png" alt="Radis Festival" class="nav-logo" />
      <h1>Le Radis Festival</h1>
    </div>


    <ul>
      <li><Button label="Infos" @click="scrollTo('about')" /></li>
      <li><Button label="Benevoles" @click="openBenevoles" /></li>
    </ul>
  </nav>
</template>

<style scoped>
.title {
  display: flex;
  align-items: center;
}

h1 {
  font-size: 2.5em;
}

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
  background-color: var(--color-beige);
  border-bottom: 3px solid var(--color-brown-dark);
  box-shadow: 0 2px 0 var(--color-brown-deep);
}

.nav-logo {
  height: 80px;
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

@media (max-width: 899px) {
  nav {
    flex-direction: column;
    gap: 20px;
    padding: 20px 0;
  }
}
</style>
