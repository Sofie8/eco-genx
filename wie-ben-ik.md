---
title: Wie ben ik?
layout: default
permalink: /over/wie-ben-ik/
---

<style>
  .wrap{
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1.25rem;
    box-sizing: border-box;
  }
  .hero{
    display:grid;
    grid-template-columns: 1.05fr 1fr;
    gap: 2rem;
    align-items: start;
    margin: 1.2rem 0 2rem;
  }
  .hero img{
    width:100%;
    height: 540px;
    object-fit: cover;
    border-radius: 18px;
    display:block;
    border: 1px solid rgba(0,0,0,.08);
    box-shadow: 0 14px 36px rgba(0,0,0,.10);
  }
  .eyebrow{
    font-size: .86rem;
    letter-spacing: .08em;
    text-transform: uppercase;
    opacity: .7;
    margin-bottom: .45rem;
  }
  h1{ margin:0 0 .6rem; font-size: 2.2rem; line-height:1.1; }
  .lead{ opacity:.86; line-height:1.7; }
  .chips{ display:flex; gap:.5rem; flex-wrap:wrap; margin: 1.1rem 0 0; }
  .chip{
    border:1px solid rgba(0,0,0,.10);
    background: rgba(9,45,38,.04);
    padding: .35rem .65rem;
    border-radius: 999px;
    font-size: .92rem;
  }
  .section{
    margin: 2.2rem 0;
    padding-top: 1.3rem;
    border-top: 1px solid rgba(0,0,0,.08);
  }
  .muted{ opacity:.82; }
  @media (max-width: 980px){
    .hero{ grid-template-columns: 1fr; }
    .hero img{ height: 360px; }
  }
</style>

<div class="wrap">

  <section class="hero">
    <div>
      <img src="{{ '/images/about-1.jpg' | relative_url }}" alt="Sofie Thijs — veldwerk en staalname">
    </div>

    <div>
      <div class="eyebrow">Concept bio</div>
      <h1>Ik ben Sofie Thijs.</h1>

      <p class="lead">
        Als doctor in de biologie en milieu-microbiologie is mijn fascinatie altijd uitgegaan naar de onzichtbare wereld van micro-organismen
        die de gezondheid van onze bodems en landschappen mee bepaalt. Mijn academische reis begon aan de Universiteit Hasselt en bracht me via
        een postdoc in bio-informatica aan de University of Waterloo in Canada terug naar waar het allemaal begon: de complexe, levende materie onder onze voeten.
      </p>

      <div class="chips">
        <span class="chip">Ecologie</span>
        <span class="chip">Microbiologie</span>
        <span class="chip">DNA/eDNA & PCR</span>
        <span class="chip">Fytotechnologie</span>
        <span class="chip">Veld ↔ labo ↔ besluitvorming</span>
      </div>
    </div>
  </section>

  <section class="section">
    <h2>Van labo naar landschap</h2>
    <p class="muted">
      Die brug tussen diepgravende wetenschap en concrete milieuproblemen is de rode draad in mijn carrière.
      Mijn focus op praktische oplossingen begon al tijdens mijn doctoraat, waarin ik de unieke eigenschappen van explosieven-etende bacteriën onderzocht
      die de springstof TNT kunnen afbreken. Dit toonde me al vroeg de immense, onontgonnen kracht van micro-organismen.
    </p>

    <p class="muted">
      Tijdens mijn postdoc werkte ik verder op het raakvlak van fundamenteel onderzoek en vele en complexe verontreinigingen zoals olie, VOCLs,
      zware metalen en PFAS. Ik zag echter ook van dichtbij hoe theoretische kennis vaak moeizaam de weg vond naar het veld.
      Daarom heb ik me toegelegd op het vertalen van wetenschap naar praktische, uitvoerbare oplossingen.
    </p>

    <p class="muted">
      Om de vinger aan de pols te houden van de nieuwste wetenschappelijke doorbraken, combineer ik mijn Eco-GenX activiteiten met een deeltijdse aanstelling (20%)
      als coördinator-navorser aan de UHasselt (Centrum voor Milieukunde). Zo was ik mede-auteur van de “Code van Goede Praktijk Fytoremediatie” (OVAM),
      een handleiding om fytoremediatie correct en efficiënt toe te passen in Vlaanderen.
    </p>
  </section>

  <section class="section">
    <h2>De noodzaak van meetbaar bewijs</h2>
    <p class="muted">
      Klassieke en bio-gebaseerde saneringen pakken vaak de symptomen aan, maar de onderliggende processen blijven een zwarte doos.
      Ik ben ervan overtuigd dat we moeten evolueren naar een aanpak waarbij we de natuurlijke processen niet alleen inzetten, maar ook sturen en meten.
    </p>

    <ul class="muted">
      <li><strong>MicroProof:</strong> via eDNA/DNA-technieken maken we zichtbaar wat er biologisch gebeurt (het “hoe en waarom”).</li>
      <li><strong>PlantIQ:</strong> de sleutel ligt in synergie: microbiële inzichten combineren met plantengenetica voor robuuste systemen.</li>
      <li><strong>Onweerlegbaar bewijs:</strong> niet alleen “saneren” of “productie”, maar een veerkrachtig biologisch systeem ontwerpen én bewijzen.</li>
    </ul>
  </section>

  <section class="section">
    <h2>Waar staat Eco-GenX voor?</h2>
    <p class="muted">
      <strong>Eco</strong> verwijst naar ecologie: het geheel van natuurlijke processen die we kunnen inzetten voor herstel en veerkracht.
      <strong>GenX</strong> verwijst naar genetica én de meetbare proof-layer (DNA/eDNA) waarmee we begrijpen wat er gebeurt, kunnen bijsturen
      en resultaten onderbouwen.
    </p>
  </section>

</div>
