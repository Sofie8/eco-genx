---
title: Home
layout: default
permalink: /
nav:
  order: 1
  tooltip: Home
---

<style>
  /* page container */
  .home-wrap{
    width: 100%;
    max-width: 1120px;
    margin: 0 auto;
    padding: 0 1.25rem;
    box-sizing: border-box;
  }

  /* FULL-WIDTH HERO (biologic/ossiado vibe) */
  .hero-full{
    position: relative;
    width: 100%;
    min-height: 520px;
    background-image: url("{{ '/images/hero.jpg' | relative_url }}");
    background-size: cover;
    background-position: center;
    border-bottom: 1px solid rgba(0,0,0,.08);
  }
  .hero-full::before{
    content:"";
    position:absolute; inset:0;
    background: linear-gradient(90deg,
      rgba(9,45,38,.78) 0%,
      rgba(9,45,38,.62) 45%,
      rgba(9,45,38,.20) 100%);
  }
  .hero-inner{
    position: relative;
    min-height: 520px;
    display: grid;
    align-items: center;
    padding: 3.2rem 0;
  }

  .kicker{
    font-size: .86rem;
    letter-spacing: .08em;
    text-transform: uppercase;
    opacity: .9;
    margin-bottom: .6rem;
    color: rgba(255,255,255,.86);
  }

  .hero-title{
    margin: 0 0 .65rem;
    font-size: 3rem;
    line-height: 1.05;
    color: #fff;
    max-width: 18ch;
  }

  .hero-quote{
    margin: .6rem 0 1.1rem;
    font-size: 1.35rem;
    line-height: 1.35;
    color: rgba(255,255,255,.92);
    max-width: 58ch;
  }

  .hero-lead{
    margin: 0;
    font-size: 1.05rem;
    line-height: 1.65;
    color: rgba(255,255,255,.84);
    max-width: 72ch;
  }

  .btnrow{
    display:flex;
    gap:.8rem;
    flex-wrap:wrap;
    margin-top: 1.4rem;
  }
  .btn{
    display:inline-flex;
    align-items:center;
    gap:.45rem;
    padding:.7rem 1.05rem;
    border-radius: 12px;
    text-decoration:none;
    border: 1px solid rgba(255,255,255,.28);
    background: rgba(255,255,255,.10);
    color: #fff;
    transition: transform .12s ease, background .12s ease, border-color .12s ease;
  }
  .btn.primary{
    background: rgba(255,255,255,.18);
    border-color: rgba(255,255,255,.36);
  }
  .btn:hover{
    transform: translateY(-1px);
    background: rgba(255,255,255,.16);
    border-color: rgba(255,255,255,.44);
  }

  /* sections */
  .section{
    margin: 2.8rem 0;
  }
  .section h2{
    margin: 0 0 .55rem;
    font-size: 1.7rem;
    line-height: 1.2;
  }
  .muted{ opacity:.86; }
  .section-intro{ max-width: 72ch; }

  /* cards */
  .cards{
    display:grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 1.2rem;
    margin-top: 1.2rem;
  }
  .card{
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    padding: 1.2rem 1.2rem 1.05rem;
    background: #fff;
    box-shadow: 0 14px 36px rgba(0,0,0,.08);
    transition: transform .12s ease, box-shadow .12s ease;
  }
  .card:hover{
    transform: translateY(-1px);
    box-shadow: 0 18px 44px rgba(0,0,0,.10);
  }
  .card h3{ margin: 0 0 .45rem; }
  .card ul{ margin: .6rem 0 0; padding-left: 1.05rem; }
  .card li{ margin: .3rem 0; }
  .card a{
    display:inline-block;
    margin-top: .9rem;
    text-decoration:none;
    border-bottom: 1px solid rgba(0,0,0,.25);
    padding-bottom: .08rem;
  }

  /* steps */
  .steps{
    display:grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 1.2rem;
    margin-top: 1.2rem;
  }
  .step{
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    padding: 1.05rem 1.15rem;
    background: #fff;
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
  }
  .step .nr{ font-weight: 700; opacity: .8; margin-bottom: .35rem; }

  /* CTA */
  .cta{
    border-radius: 20px;
    padding: 1.4rem 1.4rem;
    background: rgba(9,45,38,.06);
    border: 1px solid rgba(9,45,38,.12);
  }

  @media (max-width: 980px){
    .hero-full{ min-height: 520px; }
    .hero-inner{ padding: 2.2rem 0; }
    .hero-title{ font-size: 2.25rem; }
    .hero-quote{ font-size: 1.2rem; }
  }
</style>

<!-- FULL-WIDTH HERO -->
<section class="hero-full">
  <div class="home-wrap hero-inner">
    <div>
      <div class="kicker">Eco-GenX · consultancy</div>
      <h1 class="hero-title">Engineering nature</h1>

      <p class="hero-quote">
        <strong>Milieuvraagstuk?</strong> Ik vertaal de beste wetenschap naar oplossingen die werken in de praktijk —
        van water en bodem tot landschapsherstel.
      </p>

      <p class="hero-lead">
        Ik help je met advies en onderzoek rond nature-based oplossingen, phytotechnologie (planten, microben, gerichte additieven)
        en <em>DNA-based proof</em> om te meten en te onderbouwen wat er écht gebeurt op het terrein.
      </p>

      <div class="btnrow">
        <a class="btn primary" href="{{ '/restore/' | relative_url }}">Bekijk diensten</a>
        <a class="btn" href="{{ '/contact/' | relative_url }}">Neem contact op</a>
      </div>
    </div>
  </div>
</section>

<div class="home-wrap">

  <section class="section" id="diensten">
    <h2>Diensten</h2>
    <p class="muted section-intro">Drie domeinen die je apart kan inzetten — of combineren in één traject.</p>

    <div class="cards">
      <div class="card">
        <h3>Restore</h3>
        <p class="muted">Bodem- en waterherstel met phytoremediatie en nature-based oplossingen.</p>
        <ul>
          <li>strategie & haalbaarheidsinschatting</li>
          <li>soil/water assessment & monitoringplan</li>
          <li>hersteltrajecten voor gezonde, productieve sites</li>
        </ul>
        <a href="{{ '/restore/' | relative_url }}">Meer over Restore →</a>
      </div>

      <div class="card">
        <h3>MicroProof</h3>
        <p class="muted">DNA/PCR en eDNA om te bewijzen wat werkt — en om bij te sturen.</p>
        <ul>
          <li>eDNA monitoring & detectie</li>
          <li>verificatie van bio-producten/claims</li>
          <li>microbieel profiel & kwantificatie</li>
        </ul>
        <a href="{{ '/microproof/' | relative_url }}">Meer over MicroProof →</a>
      </div>

      <div class="card">
        <h3>PlantIQ</h3>
        <p class="muted">Plantgenetica en selectie als beslissingshulp voor robuuste teelt en herstel.</p>
        <ul>
          <li>marker-assisted selectie & screening</li>
          <li>interpretatie van genetische data</li>
          <li>advies voor keuze van soorten/rassen</li>
        </ul>
        <a href="{{ '/plantiq/' | relative_url }}">Meer over PlantIQ →</a>
      </div>
    </div>
  </section>

  <section class="section" id="aanpak">
    <h2>Eco-GenX aanpak</h2>
    <p class="muted section-intro">Eenvoudig, meetbaar en iteratief: <strong>meten → begrijpen → optimaliseren</strong>.</p>

    <div class="steps">
      <div class="step">
        <div class="nr">1 · Meten</div>
        <p class="muted">Staalname, veldobservaties en (waar zinvol) eDNA/PCR om objectief te starten.</p>
      </div>
      <div class="step">
        <div class="nr">2 · Analyseren</div>
        <p class="muted">Interpretatie en ontwerpkeuzes: wat is haalbaar, wat werkt, en wat moet je vermijden.</p>
      </div>
      <div class="step">
        <div class="nr">3 · Optimaliseren</div>
        <p class="muted">Plan of proefopzet + monitoring zodat je gericht kan bijsturen en aantonen wat werkt.</p>
      </div>
    </div>
  </section>

  <section class="section" id="projecten">
    <h2>Projecten</h2>
    <p class="muted section-intro">Een paar voorbeelden (later kan je dit uitbreiden met cases, foto’s en resultaten).</p>
    <ul>
      <li><strong>Herstelstrategie</strong> voor complexe verontreiniging met phytobenadering en monitoring.</li>
      <li><strong>Field-verificatie</strong> van bioremediatie: meten of claims kloppen met DNA-based proof.</li>
      <li><strong>Plantselectie</strong> als beslissingshulp voor robuustere toepassing op terrein/teelt.</li>
    </ul>
    <p><a href="{{ '/projects/' | relative_url }}">Bekijk projecten →</a></p>
  </section>

  <section class="section">
    <div class="cta">
      <h2>Even sparren?</h2>
      <p class="muted section-intro">
        Stuur je locatie, je vraag en (als je hebt) bestaande analyses. Dan bekijk ik wat de slimste eerste stap is.
      </p>
      <div class="btnrow">
        <a class="btn primary" href="{{ '/contact/' | relative_url }}">Contacteer mij</a>
        <a class="btn" href="{{ '/about/' | relative_url }}">Meer over Eco-GenX</a>
      </div>
    </div>
  </section>

</div>
