<script setup>
import Button from './Button.vue'
</script>

<template>
  <nav>
    <ul>
      <li>
        <Button label="Emplacement"></Button>
      </li>
      <li>
        <Button label="Programmation"></Button>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
nav ul {
  display: flex;
  justify-content: space-between;
}
</style>
