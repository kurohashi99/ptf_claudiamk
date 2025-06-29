---
title: C2M CONNEXION
publishDate: 2025-01-01 00:00:00
img: /assets/Maj flyer c2m.png
img_alt: C2M CONNEXION
description: |
  Responsable de la gestion de projet et de la conception événementielle.
tags:
  - Magasin
  - Import export
  - gestion de projet
---


## Présentation du projet

C2M Connexion est une boutique unique au Congo, née de la vision et de la détermination d’une mère et de son fils. Ensemble, ils ont créé un espace dédié à la vente de produits neufs et reconditionnés de haute qualité, offrant ainsi une alternative responsable et économique aux consommateurs.

Notre Histoire
L’histoire de C2M Connexion s’inscrit dans un engagement fort en faveur de l’innovation, de l’écologie et de la solidarité. Portés par une passion commune pour le développement durable, les fondateurs ont mis en place un circuit vertueux : des équipements sont collectés en Europe, rigoureusement triés, reconditionnés selon les normes en vigueur, puis acheminés vers le Congo-Brazzaville et le Congo-Kinshasa. Ce modèle repose sur une idée simple et forte : "Zéro déchet – dans le respect des normes

Nos Gammes de Produits
C2M Connexion propose une large sélection de produits, tous soigneusement vérifiés pour assurer performance et fiabilité :

Électroménager : Réfrigérateurs, lave-linge, fours, aspirateurs, etc.

Automobile : Voitures reconditionnées prêtes à reprendre la route.

Téléphonie : Smartphones neufs et reconditionnés à prix accessibles.

Chaque article reconditionné contribue à prolonger la durée de vie des objets tout en réduisant l’impact environnemental.

Nos Services Numériques
C2M Connexion, c’est aussi une offre digitale moderne adaptée aux besoins des particuliers, entreprises et associations :

Création de sites internet personnalisés et professionnels.

Communication digitale : gestion de réseaux sociaux, stratégie de contenu, publicité en ligne.

Graphisme : conception de logos, brochures, affiches, visuels adaptés à votre image.

Notre Engagement
En choisissant C2M Connexion, vous faites plus qu’un simple achat :
✔️ Vous soutenez une démarche écologique
✔️ Vous participez à l’économie circulaire entre l’Europe et l’Afrique
✔️ Vous favorisez un modèle de consommation éthique et durable

📍 Adresse : 133 Rue Miadeka, Ouenzé, Brazzaville

<!-- ✅ CAROUSEL -->
<div class="carousel" id="carousel">
  <div class="carousel-track" id="carousel-track">
    <div class="carousel-slide"><img src="/assets/claudiadockeur1.jpg" alt="Image 1" loading="lazy" /></div>
    <div class="carousel-slide"><img src="/assets/CLAUDIADOCK2.jpg" alt="Image 2" loading="lazy" /></div>
    <div class="carousel-slide"><img src="/assets/giftboutique.jpg" alt="Image 3" loading="lazy" /></div>
    <div class="carousel-slide"><img src="/assets/inboutique.jpg" alt="Image 4" loading="lazy" /></div>
    <div class="carousel-slide"><img src="/assets/inside.jpg" alt="Image 5" loading="lazy" /></div>
    <div class="carousel-slide"><img src="/assets/outside.jpg" alt="Image 6" loading="lazy" /></div>
  </div>

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
