---
title: Home
layout: default
permalink: /
hero_image: /images/hero-me.jpg
---

<style>
  .hero {
    display: grid;
    grid-template-columns: 1.2fr 1fr;
    gap: 2.5rem;
    align-items: center;
    margin: 1.5rem 0 2.5rem;
  }
  .hero img {
    width: 100%;
    height: auto;
    border-radius: 14px;
    display: block;
  }
  .hero h1 { margin: 0 0 .5rem; font-size: 2.4rem; line-height: 1.1; }
  .hero p  { margin: .7rem 0; font-size: 1.05rem; }
  .kicker  { opacity: .85; font-weight: 600; letter-spacing: .02em; }
  .quote   { font-size: 1.2rem; line-height: 1.35; margin: .9rem 0 1rem; }
  .btnrow  { display: flex; gap: .8rem; flex-wrap: wrap; margin-top: 1.1rem; }
  .btn     { display: inline-block; padding: .65rem 1rem; border-radius: 10px; text-decoration: none; }
  .btn.primary { background: rgba(255,255,255,.12); border: 1px solid rgba(255,255,255,.20); }
  .btn.secondary { border: 1px solid rgba(255,255,255,.20); }

  .section { margin: 2.8rem 0; }
  .section h2 { margin-bottom: .6rem; }
  .muted { opacity: .85; }

  .cards {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.1rem;
    margin-top: 1.1rem;
  }
  .card {
    border: 1px solid rgba(255,255,255,.12);
    border-radius: 14px;
    padding: 1.1rem 1.1rem 1rem;
    background: rgba(0,0,0,.08);
  }
  .card h3 { margin: 0 0 .4rem; }
  .card ul { margin: .6rem 0 0; padding-left: 1.1rem; }
  .card a { display: inline-block; margin-top: .8rem; }

  .steps {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.1rem;
    margin-top: 1.1rem;
  }
  .step {
    border: 1px solid rgba(255,255,255,.12);
    border-radius: 14px;
    padding: 1rem 1.1rem;
    background: rgba(0,0,0,.06);
  }
  .step .nr { font-weight: 700; opacity: .85; }

  .cta {
    border: 1px solid rgba(255,255,255,.16);
    border-radius: 16px;
    padding: 1.3rem 1.3rem;
    background: rgba(0,0,0,.10);
    display: grid;
    gap: .6rem;
  }

  @media (max-width: 980px) {
    .hero { grid-template-columns: 1fr; }
    .cards, .steps { grid-template-columns: 1fr; }
    .hero h1 { font-size: 2rem; }
  }
</style>

<section class="hero">
  <div>
    <img src="{{ page.hero_image | relative_url }}" alt="Veldwerk en staalname in een natuurlijke omgeving">
  </div>

  <div>
    <div class="kicker">Eco-GenX · consultancy</div>
    <h1>Engineering Nature</h1>

    <p class="quote"><strong>Milieuvraagstuk?</strong> Ik vertaal de beste wetenschap naar oplossingen die werken in de praktijk — van water en bodem tot landschapsherstel.</p>

    <p class="muted">
      Ik help je met advies en onderzoek rond nature-based oplossingen, phytotechnologie (planten, microben, gerichte additieven)
      en <em>DNA-based proof</em> om te meten en te onderbouwen wat er écht gebeurt op het terrein.
    </p>

    <div class="btnrow">
      <a class="btn primary" href="{{ '/restore/' | relative_url }}">Bekijk diensten</a>
      <a class="btn secondary" href="{{ '/contact/' | relative_url }}">Neem contact op</a>
    </div>
  </div>
</section>

<section class="section" id="diensten">
  <h2>Diensten</h2>
  <p class="muted">Drie domeinen die je apart kan inzetten — of combineren in één traject.</p>

  <div class="cards">
    <div class="card">
      <h3>Restore</h3>
      <p>Bodem- en waterherstel met phytoremediatie en nature-based oplossingen.</p>
      <ul>
        <li>strategie & haalbaarheidsinschatting</li>
        <li>soil/water assessment & monitoringplan</li>
        <li>hersteltrajecten voor gezonde, productieve sites</li>
      </ul>
      <a href="{{ '/restore/' | relative_url }}">Meer over Restore →</a>
    </div>

    <div class="card">
      <h3>MicroProof</h3>
      <p>DNA/PCR en eDNA om te bewijzen wat werkt — en om bij te sturen.</p>
      <ul>
        <li>eDNA monitoring & detectie</li>
        <li>verificatie van bio-producten/claims</li>
        <li>microbieel profiel & kwantificatie</li>
      </ul>
      <a href="{{ '/microproof/' | relative_url }}">Meer over MicroProof →</a>
    </div>

    <div class="card">
      <h3>PlantIQ</h3>
      <p>Plantgenetica en selectie als beslissingshulp voor robuuste teelt en herstel.</p>
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
  <p class="muted">Eenvoudig, meetbaar en iteratief: <strong>meten → begrijpen → optimaliseren</strong>.</p>

  <div class="steps">
    <div class="step">
      <div class="nr">1 · Meten</div>
      <p>Staalname, veldobservaties en (waar zinvol) eDNA/PCR om objectief te starten.</p>
    </div>
    <div class="step">
      <div class="nr">2 · Analyseren</div>
      <p>Interpretatie en ontwerpkeuzes: wat is haalbaar, wat werkt, en wat moet je vermijden.</p>
    </div>
    <div class="step">
      <div class="nr">3 · Optimaliseren</div>
      <p>Plan of proefopzet + monitoring zodat je gericht kan bijsturen en aantonen wat werkt.</p>
    </div>
  </div>
</section>

<section class="section" id="projecten">
  <h2>Projecten</h2>
  <p class="muted">Een paar voorbeelden (hier kan je later cases met foto’s en resultaten van maken).</p>
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
    <p class="muted">
      Stuur je locatie, je vraag en (als je hebt) bestaande analyses. Dan bekijk ik wat de slimste eerste stap is.
    </p>
    <div class="btnrow">
      <a class="btn primary" href="{{ '/contact/' | relative_url }}">Contacteer mij</a>
      <a class="btn secondary" href="{{ '/about/' | relative_url }}">Meer over Eco-GenX</a>
    </div>
  </div>
</section>

## Contact
Have a site, sample set, or question in mind?  
[Get in touch →]({{ '/contact/' | relative_url }})
