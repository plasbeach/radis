<template>
  <section class="about">
    <div class="about-inner">
      <div class="about-text">
        <h2>Le Festival</h2>
        <p>
          Le Radis Festival, c'est un rendez-vous unique au cœur de la nature, où la musique se mêle
          à la convivialité. Chaque année, des milliers de festivaliers se retrouvent pour vivre une
          expérience inoubliable, entre scènes en plein air, artistes émergents et ambiance
          électrique.
        </p>
        <p>
          Préparez-vous à plonger dans un univers décalé, coloré et savamment cultivé — comme un
          bon radis bien poussé.
        </p>
      </div>
      <div class="about-map">
        <img src="@/assets/map.png" alt="Plan du festival" />
        <span class="map-caption">Plan du site</span>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about {
  background-color: #47311e;
  color: #e5dac5;
  padding: 5rem 2rem;
}

.about-inner {
  max-width: 1100px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
}

h2 {
  font-size: clamp(2rem, 5vw, 3.5rem);
  font-weight: 900;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  margin-bottom: 1.5rem;
  color: #e5dac5;
}

p {
  font-size: clamp(1rem, 1.5vw, 1.2rem);
  line-height: 1.8;
  opacity: 0.85;
  margin-bottom: 1rem;
}

.about-map {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.75rem;
}

.about-map img {
  width: 100%;
  height: auto;
  border-radius: 8px;
  border: 4px solid #e5dac5;
  box-shadow: 8px 8px 0 rgba(0, 0, 0, 0.3);
}

.map-caption {
  font-size: 0.85rem;
  text-transform: uppercase;
  letter-spacing: 0.15em;
  opacity: 0.6;
}

@media (max-width: 700px) {
  .about-inner {
    grid-template-columns: 1fr;
    gap: 2.5rem;
  }
}
</style>