---
title: MicroProof
layout: default
permalink: /microproof/
redirect_from:
  - /MicroProof/
  - /Microproof/
nav:
  order: 2
  tooltip: MicroProof
---

<style>
  /* ---------------------------------------------------------
     MicroProof page — Full width sections + service pills
     Scoped to .svc-microproof
     --------------------------------------------------------- */

  /* Force this page content full width (theme wraps markdown) */
  main{
    max-width: none !important;
    padding: 0 !important;
    overflow: visible !important;
  }
  main > *,
  main .content,
  main article,
  main .page,
  main .post{
    max-width: none !important;
    padding: 0 !important;
    margin: 0 !important;
    overflow: visible !important;
  }

  .svc-microproof{
    --cream: #f6f4ee;
    --ink: rgba(0,0,0,.86);
    --muted: rgba(0,0,0,.68);
    --line: rgba(0,0,0,.08);
    --green: #0b3b2f;
  }

  /* Pills on top-right */
  .svc-microproof .service-topbar{
    position: absolute;
    top: 1.05rem;
    right: 1.25rem;
    z-index: 5;
  }
  @media (max-width: 980px){
    .svc-microproof .service-topbar{
      position: static;
      margin: 0;
      padding: 1rem 1.25rem 0;
      display: flex;
      justify-content: center;
    }
  }

  /* Hero */
  .svc-microproof .hero{
    position: relative;
    left: 50%;
    right: 50%;
    width: 100vw;
    margin-left: -50vw;
    margin-right: -50vw;

    background: linear-gradient(180deg, rgba(11,59,47,.92), rgba(8,42,34,.92));
    color: rgba(255,255,255,.92);
    padding: 4.6rem 0 3.2rem;
  }
  .svc-microproof .hero-inner{
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1.25rem;
    display: grid;
    grid-template-columns: 1.2fr .8fr;
    gap: 2rem;
    align-items: end;
  }
  .svc-microproof .eyebrow{
    font-size: .86rem;
    letter-spacing: .10em;
    text-transform: uppercase;
    opacity: .8;
    margin-bottom: .6rem;
  }
  .svc-microproof h1{
    margin: 0 0 .6rem;
    font-size: 3rem;
    line-height: 1.04;
    letter-spacing: .02em;
  }
  .svc-microproof .hero p{
    margin: 0;
    max-width: 72ch;
    line-height: 1.7;
    opacity: .92;
    font-size: 1.05rem;
  }

  .svc-microproof .hero-card{
    border: 1px solid rgba(255,255,255,.16);
    border-radius: 18px;
    padding: 1.05rem 1.1rem;
    background: rgba(255,255,255,.06);
    box-shadow: 0 18px 44px rgba(0,0,0,.18);
  }
  .svc-microproof .hero-card strong{ display:block; margin-bottom:.35rem; }
  .svc-microproof .hero-card ul{
    margin:.45rem 0 0;
    padding-left: 1.1rem;
    opacity:.92;
  }

  /* Full width blocks */
  .svc-microproof .block{
    position: relative;
    left: 50%;
    right: 50%;
    width: 100vw;
    margin-left: -50vw;
    margin-right: -50vw;

    display:grid;
    grid-template-columns: 1.15fr 1fr;
    min-height: 560px;
  }
  .svc-microproof .block.reverse{
    grid-template-columns: 1fr 1.15fr;
  }

  .svc-microproof .photo{
    position: relative;
    overflow:hidden;
  }
  .svc-microproof .photo img{
    width:100%;
    height:100%;
    object-fit:cover;
    display:block;
  }

  .svc-microproof .text{
    background: var(--cream);
    padding: 4.1rem 3.2rem;
    display:flex;
    flex-direction:column;
    justify-content:center;
    border-top: 1px solid var(--line);
    border-bottom: 1px solid var(--line);
  }

  .svc-microproof .text h2{
    margin: 0 0 .75rem;
    font-size: 2.25rem;
    line-height: 1.08;
    color: var(--ink);
  }
  .svc-microproof .lead{
    margin: 0 0 1.1rem;
    color: var(--muted);
    line-height: 1.75;
    max-width: 75ch;
    font-size: 1.03rem;
  }

  .svc-microproof .key{
    margin-top: .6rem;
    padding-top: 1rem;
    border-top: 1px solid rgba(0,0,0,.10);
  }
  .svc-microproof .key-title{
    font-weight: 700;
    letter-spacing: .02em;
    margin: 0 0 .5rem;
    color: var(--ink);
  }
  .svc-microproof .key ul{
    margin: .2rem 0 0;
    padding-left: 1.1rem;
    color: var(--ink);
  }
  .svc-microproof .key li{ margin: .35rem 0; }

  /* Split mini-cards (optional) */
  .svc-microproof .mini{
    display:grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1rem;
    margin-top: 1.1rem;
  }
  .svc-microproof .mini > div{
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 16px;
    padding: 1rem 1rem;
    background: rgba(255,255,255,.55);
  }
  .svc-microproof .mini h3{
    margin: 0 0 .35rem;
    font-size: 1.1rem;
  }
  .svc-microproof .mini p{
    margin: 0;
    color: var(--muted);
    line-height: 1.65;
  }

  /* CTA */
  .svc-microproof .cta{
    position: relative;
    left: 50%;
    right: 50%;
    width: 100vw;
    margin-left: -50vw;
    margin-right: -50vw;

    background: var(--green);
    color: rgba(255,255,255,.92);
    padding: 2.6rem 0;
  }
  .svc-microproof .cta-inner{
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1.25rem;
    display:flex;
    flex-wrap:wrap;
    gap: 1rem 1.4rem;
    align-items:center;
    justify-content: space-between;
  }
  .svc-microproof .cta h3{
    margin:0 0 .35rem;
    font-size: 1.6rem;
  }
  .svc-microproof .cta p{
    margin:0;
    opacity:.9;
    max-width: 70ch;
  }
  .svc-microproof .cta a{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    padding: .7rem 1rem;
    border-radius: 12px;
    border: 1px solid rgba(255,255,255,.22);
    background: rgba(255,255,255,.08);
    text-decoration:none;
    color: rgba(255,255,255,.92);
    white-space:nowrap;
  }
  .svc-microproof .cta a:hover{ background: rgba(255,255,255,.12); }

  @media (max-width: 980px){
    .svc-microproof .hero-inner{
      grid-template-columns: 1fr;
      align-items: start;
    }
    .svc-microproof h1{ font-size: 2.2rem; }
    .svc-microproof .block,
    .svc-microproof .block.reverse{
      grid-template-columns: 1fr;
      min-height: auto;
    }
    .svc-microproof .photo{ height: 340px; }
    .svc-microproof .text{ padding: 2.2rem 1.25rem; }
    .svc-microproof .text h2{ font-size: 1.85rem; }
    .svc-microproof .mini{ grid-template-columns: 1fr; }
  }
</style>

<div class="svc-microproof">

  <!-- service pills (rechtsboven) -->
  <div class="service-topbar">
    <div class="service-pills">
      <a href="{{ '/restore/' | relative_url }}">Restore</a>
      <a class="is-active" href="{{ '/microproof/' | relative_url }}">MicroProof</a>
      <a href="{{ '/plantiq/' | relative_url }}">PlantIQ</a>
    </div>
  </div>

  <!-- HERO -->
  <section class="hero">
    <div class="hero-inner">
      <div>
        <div class="eyebrow">Diensten · MicroProof</div>
        <h1>Microbiële expertise & bewijsvoering</h1>
        <p>
          Van klassieke microbiologie tot DNA-technieken: MicroProof maakt de “zwarte doos” open.
          Zo kan je volgen wat er leeft, wat actief is, en of je interventie écht doet wat ze belooft.
        </p>
      </div>

      <div class="hero-card">
        <strong>Wat je krijgt</strong>
        <ul>
          <li>DNA/eDNA, qPCR & sequencing (amplicon/shotgun)</li>
          <li>kweek & isolatie (bodem/plant)</li>
          <li>interpretatie: van data naar decision-ready conclusies</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- BLOCK 1 -->
  <section class="block">
    <div class="photo">
      <img src="{{ '/images/microproof-1.jpg' | relative_url }}" alt="Microbiologie van de bodem">
    </div>

    <div class="text">
      <h2>1) Microbiologie van de bodem</h2>
      <p class="lead">
        Bodems functioneren dankzij hun microbiële gemeenschap. Door diversiteit, verhouding schimmels/bacteriën
        en functionele indicatoren te meten, krijg je zicht op de biologische vitaliteit en de interacties plant–bodem.
      </p>

      <div class="mini">
        <div>
          <h3>Biologische activiteit</h3>
          <p>Indicatoren voor vitaliteit, stress en herstelpotentieel.</p>
        </div>
        <div>
          <h3>Community structuur</h3>
          <p>Diversiteit en ratio’s (bv. schimmels/bacteriën) als sleutels tot interpretatie.</p>
        </div>
      </div>

      <div class="key">
        <div class="key-title">Typische methodes</div>
        <ul>
          <li>Community profiling (amplicon sequencing, eDNA)</li>
          <li>qPCR voor doelgroepen/genen (functionele merkers)</li>
          <li>Biolog EcoPlate (optioneel, als functionele fingerprint)</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- BLOCK 2 -->
  <section class="block reverse">
    <div class="text">
      <h2>2) Microbiologie van de plant</h2>
      <p class="lead">
        Planten zijn geen “losse organismen” maar holobionten: hun gezondheid hangt samen met microben
        in de rhizosfeer, endosfeer en fyllosfeer. MicroProof helpt om die interacties te begrijpen en te sturen.
      </p>

      <div class="key">
        <div class="key-title">Zones die we bekijken</div>
        <ul>
          <li><strong>Rhizosfeer</strong> (wortelzone) — interacties bodem–wortel</li>
          <li><strong>Endosfeer</strong> — endofytische bacteriën/schimmels</li>
          <li><strong>Fyllosfeer</strong> — bladmicrobiome & stressrespons</li>
        </ul>
      </div>

      <div class="key">
        <div class="key-title">Toepassingen</div>
        <ul>
          <li>gezondheids- en stressdiagnostiek</li>
          <li>selectie/validatie van bio-inoculanten</li>
          <li>monitoring van interventies (veld of serre)</li>
        </ul>
      </div>
    </div>

    <div class="photo">
      <img src="{{ '/images/microproof-2.jpg' | relative_url }}" alt="Microbiologie van de plant: rhizosfeer, endosfeer, fyllosfeer">
    </div>
  </section>

  <!-- BLOCK 3 -->
  <section class="block">
    <div class="photo">
      <img src="{{ '/images/microproof-3.jpg' | relative_url }}" alt="Tracking van micro-organismen met qPCR en sequencing">
    </div>

    <div class="text">
      <h2>3) Tracking van micro-organismen</h2>
      <p class="lead">
        Wil je weten of een specifieke groep microben aanwezig is, toeneemt, of actief betrokken is bij afbraak of plantgezondheid?
        Dan combineren we gerichte merkers met kwantificatie en sequencing.
      </p>

      <div class="key">
        <div class="key-title">Key methods</div>
        <ul>
          <li>qPCR / ddPCR voor kwantificatie</li>
          <li>Amplicon sequencing (bv. MinION) voor snelle community inzichten</li>
          <li>Functionele gen-merkers om “wat doet het?” te beantwoorden</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- CTA -->
  <section class="cta">
    <div class="cta-inner">
      <div>
        <h3>MicroProof inzetten op jouw site?</h3>
        <p>Stuur je vraag + type staal (bodem/plant/water) en doel (monitoring, bewijs, screening). Dan stel ik een meetplan voor.</p>
      </div>
      <a href="{{ '/contact/' | relative_url }}">Contacteer mij →</a>
    </div>
  </section>

</div>
