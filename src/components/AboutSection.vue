<template>
  <section id="about" class="about">
    <div class="about-inner">
      <div class="about-text">
        <h2>Le Festival</h2>
        <p>
          Le Radis Festival s’inspire des grandes manifestations musicales suisses, tout en
          se développant à une échelle volontairement locale. L’objectif est de proposer
          un événement culturel accessible, mettant en valeur les artistes de la région et
          favorisant la vie communautaire.
        </p>
        <p>
          Organisé par une équipe de bénévoles engagés, le festival se déroulera sur
          deux jours et accueillera une programmation musicale composée
          exclusivement d’artistes régionaux. Une buvette ainsi qu’un point de petite
          restauration seront proposés sur place. Un espace de camping sera également
          mis à disposition pour les festivaliers souhaitant dormir sur le site.
        </p>
          <p>
            L’entrée est gratuite, afin de garantir un accès équitable à toutes et tous.
          </p>
        <p>
          Préparez-vous à plonger dans un univers décalé, coloré et savamment cultivé ... comme un
          bon radis bien poussé !
        </p>
      </div>
      <div class="about-map">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2728.537636292693!2d7.109682576980919!3d46.852791171130534!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x478e6d002588099f%3A0xfa248a90bcf90ac2!2sLe%20Radis%20Festival!5e0!3m2!1sen!2sch!4v1775217975509!5m2!1sen!2sch"
          allowfullscreen
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
        ></iframe>
        <span class="map-caption">Localisation</span>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about {
  background-color: var(--color-brown-dark);
  color: var(--color-beige);
  padding: 5rem 2rem;
  scroll-margin-top: 75px;
}

.about-inner {
  max-width: 1100px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 4rem;
  align-items: stretch;
}

h2 {
  font-size: clamp(2rem, 5vw, 3.5rem);
  font-weight: 900;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  margin-bottom: 1.5rem;
  color: var(--color-beige);
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

.about-map iframe {
  width: 100%;
  height: 600px;
  border-radius: 8px;
  border: 4px solid var(--color-beige);
  box-shadow: 8px 8px 0 rgba(0, 0, 0, 0.3);
}

.map-caption {
  font-size: 0.85rem;
  text-transform: uppercase;
  letter-spacing: 0.15em;
  opacity: 0.6;
}

</style>