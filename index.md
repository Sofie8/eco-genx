---
title: Home
layout: default
permalink: /
hero_image: /images/hero.jpg
---

<style>
  /* ---------- page container ---------- */
  .home-wrap{
    width: 100%;
    max-width: 1120px;
    margin: 0 auto;
    padding: 1.25rem 1.25rem 2.5rem;
    box-sizing: border-box;
  }

  /* ---------- typography helpers ---------- */
  .muted { opacity: .86; }
  .lead  { font-size: 1.08rem; line-height: 1.65; max-width: 60ch; }
  .section-intro { max-width: 72ch; }

  /* ---------- hero ---------- */
  .hero{
    display: grid;
    grid-template-columns: 1.15fr 1fr;
    gap: 2.25rem;
    align-items: center;
    padding: 1rem 0 1.5rem;
  }

  .hero-media{
    border-radius: 18px;
    overflow: hidden;
    border: 1px solid rgba(255,255,255,.14);
    background: rgba(0,0,0,.06);
    box-shadow: 0 14px 36px rgba(0,0,0,.18);
  }

  .hero-media img{
    width: 100%;
    height: 420px;
    object-fit: cover;
    display: block;
  }

  .kicker{
    font-size: .86rem;
    letter-spacing: .06em;
    text-transform: uppercase;
    opacity: .85;
    margin-bottom: .4rem;
  }

  .hero h1{
    margin: 0 0 .55rem;
    font-size: 2.45rem;
    line-height: 1.08;
  }

  .quote{
    font-size: 1.2rem;
    line-height: 1.35;
    margin: .7rem 0 1rem;
    max-width: 55ch;
  }

  .btnrow{
    display: flex;
    gap: .8rem;
    flex-wrap: wrap;
    margin-top: 1.15rem;
  }

  .btn{
    display: inline-flex;
    align-items: center;
    gap: .45rem;
    padding: .65rem 1rem;
    border-radius: 12px;
    text-decoration: none;
    border: 1px solid rgba(255,255,255,.22);
    background: rgba(255,255,255,.06);
    transition: transform .12s ease, background .12s ease, border-color .12s ease;
  }

  .btn.primary{
    background: rgba(255,255,255,.14);
    border-color: rgba(255,255,255,.28);
  }

  .btn:hover{
    transform: translateY(-1px);
    background: rgba(255,255,255,.12);
    border-color: rgba(255,255,255,.34);
  }

  /* ---------- sections ---------- */
  .section{
    margin: 2.6rem 0;
    padding-top: 1.2rem;
    border-top: 1px solid rgba(255,255,255,.10);
  }

  .section h2{
    margin: 0 0 .55rem;
    font-size: 1.6rem;
    line-height: 1.2;
  }

  /* ---------- cards grid ---------- */
  .cards{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 1.15rem;
    margin-top: 1.2rem;
  }

  .card{
    border: 1px solid rgba(255,255,255,.12);
    border-radius: 16px;
    padding: 1.15rem 1.15rem 1rem;
    background: rgba(0,0,0,.07);
    box-shadow: 0 10px 26px rgba(0,0,0,.12);
    transition: transform .12s ease, border-color .12s ease, background .12s ease;
    height: 100%;
  }

  .card:hover{
    transform: translateY(-1px);
    border-color: rgba(255,255,255,.22);
    background: rgba(0,0,0,.09);
  }

  .card h3{ margin: 0 0 .45rem; font-size: 1.18rem; }
  .card p { margin: .35rem 0 .6rem; }

  .card ul{
    margin: .5rem 0 0;
    padding-left: 1.05rem;
  }

  .card li{ margin: .28rem 0; }

  .card a{
    display: inline-block;
    margin-top: .85rem;
    text-decoration: none;
    border-bottom: 1px solid rgba(255,255,255,.25);
    padding-bottom: .1rem;
  }

  /* ---------- steps ---------- */
  .steps{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 1.15rem;
    margin-top: 1.2rem;
  }

  .step{
    border: 1px solid rgba(255,255,255,.12);
    border-radius: 16px;
    padding: 1rem 1.1rem;
    background: rgba(0,0,0,.06);
  }

  .step .nr{
    font-weight: 700;
    opacity: .9;
    margin-bottom: .35rem;
  }

  /* ---------- CTA ---------- */
  .cta{
    border: 1px solid rgba(255,255,255,.16);
    border-radius: 18px;
    padding: 1.35rem 1.35rem;
    background: rgba(0,0,0,.10);
    box-shadow: 0 12px 32px rgba(0,0,0,.14);
  }

  /* ---------- responsive ---------- */
  @media (max-width: 980px){
    .hero{ grid-template-columns: 1fr; }
    .hero-media img{ height: 320px; }
    .hero h1{ font-size: 2.05rem; }
  }
</style>

<div class="home-wrap">

  <section class="hero">
    <div class="hero-media">
      <img src="{{ page.hero_image | relative_url }}" alt="Veldwerk en staalname in een natuurlijke omgeving">
    </div>

    <div>
      <div class="kicker">Eco-GenX · consultancy</div>
      <h1>Engineering Nature</h1>

      <p class="quote"><strong>Milieuvraagstuk?</strong> Ik vertaal de beste wetenschap naar oplossingen die werken in de praktijk — van water en bodem tot landschapsherstel.</p>

      <p class="lead muted">
        Ik help je met advies en onderzoek rond nature-based oplossingen, phytotechnologie (planten, microben, gerichte additieven)
        en <em>DNA-based proof</em> om te meten en te onderbouwen wat er écht gebeurt op het terrein.
      </p>

      <div class="btnrow">
        <a class="btn primary" href="{{ '/restore/' | relative_url }}">Bekijk diensten</a>
        <a class="btn" href="{{ '/contact/' | relative_url }}">Neem contact op</a>
      </div>
    </div>
  </section>

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
