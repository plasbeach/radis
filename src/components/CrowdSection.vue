<template>
  <section class="crowd">
    <img class="crowd-photo" src="@/assets/crowd.png" alt="Festival crowd" />
    <div class="crowd-overlay">
      <h2>Une expérience hors du commun</h2>
      <p>Des milliers de festivaliers, une seule famille.</p>
    </div>
  </section>
</template>

<style scoped>
.crowd {
  position: relative;
  width: 100%;
  overflow: hidden;
  min-height: 500px;
}

.crowd-photo {
  width: 100%;
  height: 600px;
  object-fit: cover;
  object-position: center;
  display: block;
  filter: brightness(0.6);
}

.crowd-overlay {
  position: absolute;
  inset: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: #e5dac5;
  padding: 2rem;
}

h2 {
  font-size: clamp(2rem, 5vw, 4rem);
  font-weight: 900;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  text-shadow: 0 4px 20px rgba(0, 0, 0, 0.6);
  margin-bottom: 1rem;
}

p {
  font-size: clamp(1rem, 2vw, 1.4rem);
  font-weight: 600;
  letter-spacing: 0.1em;
  text-shadow: 0 2px 8px rgba(0, 0, 0, 0.6);
  opacity: 0.9;
}
</style>
