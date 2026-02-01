---
title: Home
layout: default
permalink: /
nav:
  order: 1
  tooltip: Home
---

<style>
  /* =======================================================
     Home page (final) — relies on global assets/css/site.css
     ======================================================= */

  /* Container for inner content blocks */
  .home-wrap{
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1.25rem;
    box-sizing: border-box;
  }

  /* ---------- HERO (full-bleed) ---------- */
  .hero-full{
    position: relative;
    min-height: 560px;
    background-image: url("{{ '/images/hero.jpg' | relative_url }}");
    background-size: cover;
    background-position: center;
  }

  /* overlay for readability */
  .hero-full::before{
    content:"";
    position:absolute; inset:0;
    background:
      linear-gradient(90deg,
        rgba(9,45,38,.86) 0%,
        rgba(9,45,38,.66) 45%,
        rgba(9,45,38,.22) 100%);
  }

  .hero-inner{
    position: relative;
    min-height: 560px;
    display: grid;
    align-items: center;
    padding: 3.2rem 0;
  }

  .kicker{
    font-size: .86rem;
    letter-spacing: .08em;
    text-transform: uppercase;
    opacity: .92;
    margin-bottom: .7rem;
    color: rgba(255,255,255,.86);
  }

  .hero-title{
    margin: 0 0 .65rem;
    font-size: 3.15rem;
    line-height: 1.03;
    color: #fff;
    max-width: 18ch;
  }

  .hero-quote{
    margin: .65rem 0 1.15rem;
    font-size: 1.45rem;
    line-height: 1.35;
    color: rgba(255,255,255,.92);
    max-width: 62ch;
  }

  .hero-lead{
    margin: 0;
    font-size: 1.05rem;
    line-height: 1.65;
    color: rgba(255,255,255,.84);
    max-width: 76ch;
  }

  .btnrow{
    display:flex;
    gap:.85rem;
    flex-wrap:wrap;
    margin-top: 1.4rem;
  }

  .btn{
    display:inline-flex;
    align-items:center;
    gap:.45rem;
    padding:.75rem 1.1rem;
    border-radius: 12px;
    text-decoration:none;
    border: 1px solid rgba(255,255,255,.28);
    background: rgba(255,255,255,.10);
    color: #fff;
    transition: transform .12s ease, background .12s ease, border-color .12s ease;
  }

  .btn.primary{
    background: rgba(255,255,255,.18);
    border-color: rgba(255,255,255,.38);
  }

  .btn:hover{
    transform: translateY(-1px);
    background: rgba(255,255,255,.16);
    border-color: rgba(255,255,255,.46);
  }

  /* ---------- SECTION BASE ---------- */
  .section{
    margin: 3.1rem 0;
  }

  .section h2{
    margin: 0 0 .55rem;
    font-size: 1.75rem;
    line-height: 1.2;
  }

  .section-intro{
    max-width: 78ch;
    opacity: .86;
  }

  /* Cards / steps styling (pairs with site.css) */
  .cards, .steps{
    display:grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 1.4rem;
    margin-top: 1.25rem;
  }

  .card, .step{
    background: #fff;
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 20px;
    box-shadow: 0 14px 36px rgba(0,0,0,.08);
  }

  .card{
    padding: 1.35rem 1.35rem 1.2rem;
    transition: transform .12s ease, box-shadow .12s ease;
  }
  .card:hover{
    transform: translateY(-1px);
    box-shadow: 0 18px 44px rgba(0,0,0,.10);
  }

  .card h3{
    margin: 0 0 .5rem;
    font-size: 1.25rem;
  }

  .card p{
    margin: .35rem 0 .65rem;
    opacity: .82;
  }

  .card ul{
    margin: .6rem 0 0;
    padding-left: 1.1rem;
  }
  .card li{ margin: .3rem 0; }

  .card a{
    display:inline-block;
    margin-top: .95rem;
    text-decoration:none;
    border-bottom: 1px solid rgba(0,0,0,.28);
    padding-bottom: .08rem;
  }

  .step{
    padding: 1.1rem 1.2rem;
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
  }
  .step .nr{
    font-weight: 700;
    opacity: .85;
    margin-bottom: .35rem;
  }

  /* CTA */
  .cta{
    border-radius: 22px;
    padding: 1.5rem 1.5rem;
    background: rgba(9,45,38,.06);
    border: 1px solid rgba(9,45,38,.12);
  }

  /* Responsive hero */
  @media (max-width: 980px){
    .hero-full{ min-height: 540px; }
    .hero-inner{ min-height: 540px; padding: 2.4rem 0; }
    .hero-title{ font-size: 2.35rem; }
    .hero-quote{ font-size: 1.22rem; }
  }
</style>

<!-- HERO (full width) -->
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
    <p class="section-intro">Drie domeinen die je apart kan inzetten — of combineren in één traject.</p>

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
    <p class="section-intro">Eenvoudig, meetbaar en iteratief: <strong>meten → begrijpen → optimaliseren</strong>.</p>

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
    <p class="section-intro">Een paar voorbeelden (later kan je dit uitbreiden met cases, foto’s en resultaten).</p>
    <ul>
      <li><strong>Herstelstrategie</strong> voor complexe verontreiniging met phytobenadering en monitoring.</li>
      <li><strong>Field-verificatie</strong> van bioremediatie: meten of claims kloppen met DNA-based proof.</li>
      <li><strong>Plantselectie</strong> als beslissingshulp voor robuustere toepassing op terrein/teelt.</li>
    </ul>
    <p><a href="{{ '/projects/' | relative_url }}">Bekijk projecten →</a></p>
  </section>

  <section class="section">
    <div class="cta">
      <h2>Meetbaar bewijs</h2>
      <p class="section-intro">
        Ik combineer veldwerk, labo en data om onzekerheid weg te nemen.
        Geen ‘mooie belofte’, maar resultaten waar je beslissingen op kan nemen.
      </p>
      <div class="btnrow">
        <a class="btn primary" href="{{ '/contact/' | relative_url }}">Contacteer mij</a>
        <a class="btn" href="{{ '/over/missie-visie/' | relative_url }}">Missie & visie</a>
      </div>
    </div>
  </section>

</div>

<!-- Full-bleed proof block (uses your global .full-bleed helper in site.css) -->
<div class="full-bleed">
  <div class="grid-2x2">
    <div class="cell photo">
      <img src="{{ '/images/cert-1.jpg' | relative_url }}" alt="Analytische kwaliteit & meetbaar bewijs">
    </div>
    <div class="cell text">
      <h2>Meetbaar bewijs, decision-ready advies.</h2>
      <p>
        Ik combineer fieldwork, labo en data om onzekerheid weg te nemen.
        Geen ‘mooie belofte’, maar een aanpak die je kan verantwoorden — technisch én praktisch.
      </p>
      <p>
        Van staalname en interpretatie tot monitoring en bijsturing: je krijgt duidelijke stappen en heldere conclusies.
      </p>
      <p>
        <a href="{{ '/contact/' | relative_url }}">Even afstemmen →</a>
      </p>
    </div>
  </div>
</div>
<style>
  /* =======================================================
     Certified block (Home) — 2x2 grid zoals je voorbeeld
     ======================================================= */
  .cert-wrap{
    position: relative;
    left: 50%;
    right: 50%;
    width: 100vw;
    margin-left: -50vw;
    margin-right: -50vw;

    background: #fff;
    border-top: 1px solid rgba(0,0,0,.06);
    border-bottom: 1px solid rgba(0,0,0,.06);
  }

  .cert-grid{
    display: grid;
    grid-template-columns: 1fr 1fr;
  }

  .cert-cell{
    min-height: 360px;
  }

  .cert-photo{
    position: relative;
    overflow: hidden;
  }
  .cert-photo img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
  }

  .cert-text{
    padding: 3.2rem 3rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .cert-eyebrow{
    font-size: .85rem;
    letter-spacing: .10em;
    text-transform: uppercase;
    opacity: .75;
    margin-bottom: .75rem;
  }

  .cert-text h2{
    margin: 0 0 1rem;
    font-size: 1.9rem;
    line-height: 1.12;
  }

  .cert-text p{
    margin: 0 0 .9rem;
    line-height: 1.7;
    opacity: .86;
    max-width: 68ch;
  }

  .cert-link{
    margin-top: .6rem;
    font-weight: 600;
    text-decoration: none;
    color: rgba(11,59,47,.92);
    border-bottom: 1px solid rgba(11,59,47,.35);
    align-self: flex-start;
    padding-bottom: .08rem;
  }

  /* mobile */
  @media (max-width: 980px){
    .cert-grid{ grid-template-columns: 1fr; }
    .cert-text{ padding: 2.1rem 1.25rem; }
    .cert-cell{ min-height: unset; }
    .cert-photo{ height: 320px; }
  }
</style>

<section class="cert-wrap" aria-label="Gecertificeerde kwaliteit">
  <div class="cert-grid">

    <!-- 1) FOTO linksboven -->
    <div class="cert-cell cert-photo">
      <img src="{{ '/images/cert-1.jpg' | relative_url }}" alt="Staalnames en analytische kwaliteitsaanpak">
    </div>

    <!-- 2) TEKST rechtsboven -->
    <div class="cert-cell cert-text">
      <div class="cert-eyebrow">Gecertificeerde kwaliteitsaanpak</div>
      <h2>Meetbaar bewijs — decision-ready advies</h2>
      <p>
        Eco-GenX combineert veldwerk, labo en data om onzekerheid weg te nemen.
        Niet “mooie beloftes”, maar onderbouwde conclusies die je kan verdedigen —
        technisch én praktisch.
      </p>
      <p>
        Van staalname en interpretatie tot monitoring en bijsturing: je krijgt duidelijke
        stappen en een aanpak die reproduceerbaar is.
      </p>
      <a class="cert-link" href="{{ '/certificaten/' | relative_url }}">Bekijk certificaten →</a>
    </div>

    <!-- 3) TEKST linksonder -->
    <div class="cert-cell cert-text">
      <div class="cert-eyebrow">Analytische expertise</div>
      <h2>Kwaliteit die je project versnelt</h2>
      <p>
        Door slim te meten (multi-line-of-evidence) kan je sneller beslissen:
        wat werkt, waar zit het risico, en welke interventie levert het meeste effect.
      </p>
      <p>
        Ideaal voor bodemherstel, fytoremediatie, monitoring van natuurlijke attenuatie
        en verificatie van bio-claims.
      </p>
      <a class="cert-link" href="{{ '/contact/' | relative_url }}">Even sparren →</a>
    </div>

    <!-- 4) FOTO rechtsonder -->
    <div class="cert-cell cert-photo">
      <img src="{{ '/images/cert-2.jpg' | relative_url }}" alt="Laboratoriumanalyse en pipetteren">
    </div>

  </div>
</section>
