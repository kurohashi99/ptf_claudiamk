---
title: C2M CONNEXION SERVICE
publishDate: 2025-01-01 00:00:00
img: ./assets/all paneau.jpg
img_alt: C2M CONNEXION
description: |
  C2M CONNEXION SOCIETE DE PRESTATION DE SERVICE 
tags:
  - Magasin
  - Conciergerie
  - Prestation de service
---


## Présentation du projet - Services de Conciergerie et Consulting
C2M Connexion ne se limite pas à la vente de produits neufs et reconditionnés : la société développe également une branche dédiée aux services de conciergerie et de consulting pour les entreprises. Cette activité s’inscrit dans la même vision d’excellence et de responsabilité qui guide toute la structure.

Notre offre de services
Pensée pour répondre aux besoins quotidiens des professionnels, notre conciergerie propose un accompagnement complet et flexible :

Services de ménage et entretien : un environnement de travail propre et sain, assuré par une équipe qualifiée.

Gestion administrative et logistique : optimisation des tâches pour libérer du temps et se concentrer sur le cœur de métier.

Consulting opérationnel : conseils personnalisés pour améliorer l’organisation interne, la gestion des ressources et la communication.

Services sur mesure : assistance événementielle, accueil, gestion des urgences, et bien plus selon les besoins spécifiques de chaque entreprise.

Notre approche
Portée par la même rigueur et le souci de qualité que notre boutique, cette branche concilie professionnalisme et proximité. Nous accompagnons les entreprises dans leur développement, en apportant des solutions adaptées, fiables et durables.

Pourquoi choisir C2M Connexion Services ?
Expertise locale et internationale : une équipe formée et sensibilisée aux enjeux du contexte congolais.

Flexibilité et écoute : des prestations modulables, au plus près de vos attentes.

Engagement qualité : respect des normes, transparence et suivi régulier.

📍 Retrouvez-nous au 133 Rue Miadeka, Ouenzé, Brazzaville — votre partenaire de confiance pour simplifier votre quotidien professionnel.



<!-- ✅ CAROUSEL -->
<div class="carousel" id="carousel">
  <div class="carousel-track" id="carousel-track">
    <div class="carousel-slide"><img src="./public/assets/all pangieau.jpg" alt="Image 1" loading="lazy" /></div>
    <div class="carousel-slide"><img src="./assets/conciergerie.jpg" alt="Image 2" loading="lazy" /></div>
    <div class="carousel-slide"><img src="./assets/produit.jpg" alt="Image 3" loading="lazy" /></div>
    <div class="carousel-slide"><img src="./assets/tish shirt.jpg" alt="Image 4" loading="lazy" /></div>
  </div>
&z
  <div class="carousel-buttons">
    <button class="carousel-button" id="prev">&#10094;</button>
    <button class="carousel-button" id="next">&#10095;</button>
  </div>

  <div class="carousel-dots" id="carousel-dots"></div>
</div>

<!-- ✅ STYLES -->
<style>
  .carousel {
    position: relative;
    overflow: hidden;
    max-width: 600px;
    margin: 2rem auto;
    border-radius: 1rem;
  }

  .carousel-track {
    display: flex;
    transition: transform 0.5s ease;
  }

  .carousel-slide {
    min-width: 100%;
  }

  .carousel-slide img {
    width: 100%;
    height: auto;
    border-radius: 1rem;
  }

  .carousel-buttons {
    position: absolute;
    top: 50%;
    width: 100%;
    display: flex;
    justify-content: space-between;
    padding: 0 1rem;
    transform: translateY(-50%);
  }

  .carousel-button {
    background: rgba(0, 0, 0, 0.4);
    color: white;
    border: none;
    padding: 0.5rem 1rem;
    border-radius: 50%;
    font-size: 1.5rem;
    cursor: pointer;
  }

  .carousel-dots {
    display: flex;
    justify-content: center;
    margin-top: 1rem;
    gap: 0.5rem;
  }

  .carousel-dot {
    width: 10px;
    height: 10px;
    background: gray;
    border-radius: 50%;
    cursor: pointer;
  }

  .carousel-dot.active {
    background: blue;
  }
</style>

<!-- ✅ SCRIPT -->
<script type="module">
  const track = document.getElementById("carousel-track");
  const slides = document.querySelectorAll(".carousel-slide");
  const dotsContainer = document.getElementById("carousel-dots");
  const prev = document.getElementById("prev");
  const next = document.getElementById("next");

  let index = 0;
  const total = slides.length;

  // Generate dots
  for (let i = 0; i < total; i++) {
    const dot = document.createElement("div");
    dot.classList.add("carousel-dot");
    dot.dataset.index = i;
    dotsContainer.appendChild(dot);
  }

  const dots = document.querySelectorAll(".carousel-dot");

  function updateCarousel() {
    track.style.transform = `translateX(-${index * 100}%)`;
    dots.forEach((dot, i) => dot.classList.toggle("active", i === index));
  }

  prev.addEventListener("click", () => {
    index = (index - 1 + total) % total;
    updateCarousel();
  });

  next.addEventListener("click", () => {
    index = (index + 1) % total;
    updateCarousel();
  });

  dots.forEach((dot) => {
    dot.addEventListener("click", (e) => {
      index = Number(e.target.dataset.index);
      updateCarousel();
    });
  });

  updateCarousel();
</script>
