---
title: Restore
layout: default
permalink: /restore/
nav:
  order: 1
  tooltip: Restore
---

<style>
  /* =========================================================
     RESTORE — full width service page (no white band on top)
     Scoped to .svc-restore
     ========================================================= */

  /* 1) neutraliseer theme container/padding die de "witte band" veroorzaakt */
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

  .svc-restore{
    --cream: #f6f4ee;
    --ink: rgba(0,0,0,.88);
    --muted: rgba(0,0,0,.68);
    --line: rgba(0,0,0,.08);
    --eco-dark: #0b3b2f;
    --eco-dark-2: #082a22;
  }

  /* HERO full-bleed */
  .svc-restore .hero{
    position: relative;
    left: 50%;
    right: 50%;
    width: 100vw;
    margin-left: -50vw;
    margin-right: -50vw;

    /* 2) dit haalt de resterende “band” weg (main had vroeger 2.5rem) */
    margin-top: -2.5rem;

    background: linear-gradient(180deg, rgba(11,59,47,.92), rgba(8,42,34,.92));
    color: rgba(255,255,255,.92);
    padding: 4.2rem 0 3.2rem;
  }

  .svc-restore .hero-inner{
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1.25rem;
    display: grid;
    grid-template-columns: 1.2fr .8fr;
    gap: 2rem;
    align-items: end;
  }

  .svc-restore .eyebrow{
    font-size: .86rem;
    letter-spacing: .10em;
    text-transform: uppercase;
    opacity: .82;
    margin-bottom: .6rem;
  }

  .svc-restore h1{
    margin: 0 0 .7rem;
    font-size: 3rem;
    line-height: 1.05;
    letter-spacing: .02em;
  }

  .svc-restore .hero p{
    margin: 0;
    max-width: 72ch;
    line-height: 1.7;
    opacity: .93;
    font-size: 1.05rem;
  }

  .svc-restore .hero-card{
    border: 1px solid rgba(255,255,255,.16);
    border-radius: 18px;
    padding: 1.05rem 1.1rem;
    background: rgba(255,255,255,.06);
    box-shadow: 0 18px 44px rgba(0,0,0,.18);
  }
  .svc-restore .hero-card strong{ display:block; margin-bottom:.35rem; }
  .svc-restore .hero-card ul{
    margin:.45rem 0 0;
    padding-left: 1.1rem;
    opacity:.92;
  }
  .svc-restore .hero-card li{ margin:.35rem 0; }

  /* Full width content blocks */
  .svc-restore .block{
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
  .svc-restore .block.reverse{
    grid-template-columns: 1fr 1.15fr;
  }

  .svc-restore .photo{
    position: relative;
    overflow:hidden;
  }
  .svc-restore .photo img{
    width:100%;
    height:100%;
    object-fit:cover;
    display:block;
  }

  .svc-restore .text{
    background: var(--cream);
    padding: 4.1rem 3.2rem;
    display:flex;
    flex-direction:column;
    justify-content:center;
    border-top: 1px solid var(--line);
    border-bottom: 1px solid var(--line);
  }

  .svc-restore .text h2{
    margin: 0 0 .75rem;
    font-size: 2.25rem;
    line-height: 1.10;
    color: var(--ink);
  }

  .svc-restore .lead{
    margin: 0 0 1.15rem;
    color: var(--muted);
    line-height: 1.75;
    max-width: 75ch;
    font-size: 1.03rem;
  }

  .svc-restore .key{
    margin-top: .6rem;
    padding-top: 1rem;
    border-top: 1px solid rgba(0,0,0,.10);
  }
  .svc-restore .key-title{
    font-weight: 700;
    letter-spacing: .02em;
    margin: 0 0 .5rem;
    color: var(--ink);
  }
  .svc-restore .key ul{
    margin: .2rem 0 0;
    padding-left: 1.1rem;
    color: var(--ink);
  }
  .svc-restore .key li{ margin: .35rem 0; }

  /* CTA */
  .svc-restore .cta{
    position: relative;
    left: 50%;
    right: 50%;
    width: 100vw;
    margin-left: -50vw;
    margin-right: -50vw;

    background: var(--eco-dark);
    color: rgba(255,255,255,.92);
    padding: 2.6rem 0;
  }
  .svc-restore .cta-inner{
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1.25rem;
    display:flex;
    flex-wrap:wrap;
    gap: 1rem 1.4rem;
    align-items:center;
    justify-content: space-between;
  }
  .svc-restore .cta h3{
    margin:0 0 .35rem;
    font-size: 1.6rem;
  }
  .svc-restore .cta p{
    margin:0;
    opacity:.9;
    max-width: 72ch;
  }
  .svc-restore .cta a{
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
  .svc-restore .cta a:hover{ background: rgba(255,255,255,.12); }

  @media (max-width: 980px){
    .svc-restore .hero-inner{
      grid-template-columns: 1fr;
      align-items: start;
    }
    .svc-restore h1{ font-size: 2.2rem; }
    .svc-restore .block,
    .svc-restore .block.reverse{
      grid-template-columns: 1fr;
      min-height: auto;
    }
    .svc-restore .photo{ height: 340px; }
    .svc-restore .text{ padding: 2.2rem 1.25rem; }
    .svc-restore .text h2{ font-size: 1.85rem; }
  }
</style>

<div class="svc-restore">

  <!-- HERO -->
  <section class="hero">
    <div class="hero-inner">
      <div>
        <div class="eyebrow">Diensten · Restore</div>
        <h1>Herstel van bodem, water & landschap</h1>
        <p>
          Ik ontwerp en begeleid fytoremediatie en nature-based hersteltrajecten —
          met meetbaar bewijs, slimme monitoring en duidelijke beslissingspunten.
        </p>
      </div>

      <div class="hero-card">
        <strong>Waar Restore op focust</strong>
        <ul>
          <li>fytoremediatie & nature-based strategie</li>
          <li>site- & risico-inschatting</li>
          <li>stalen, monitoring & bewijsvoering</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- BLOCK 1 -->
  <section class="block">
    <div class="photo">
      <img src="{{ '/images/restore-1.jpg' | relative_url }}" alt="Tools om microbiële afbraak te beoordelen">
    </div>

    <div class="text">
      <h2>Tools to assess microbial biodegradation potential & activity</h2>
      <p class="lead">
        De interacties tussen planten, microben en enzymen zijn de motor van duurzaam bodemherstel en productieve gewassen.
        Klassieke chemische analyses geven slechts een momentopname en kunnen een daling in concentraties niet eenduidig
        toeschrijven aan biologische afbraak.
      </p>
      <p class="lead">
        Om te bewijzen dat de biologische motor effectief draait en de sanering duurzaam is, hanteren we een
        <strong>multi-line-of-evidence</strong> aanpak. We combineren geavanceerde DNA-technieken (eDNA) en fytoforensics
        met chemische analyses die afbraakprocessen traceren.
      </p>

      <div class="key">
        <div class="key-title">Key methods</div>
        <ul>
          <li>Molecular genetic analysis (shotgun, amplicon, eDNA, qPCR)</li>
          <li>Laboratory microcosms met/zonder isotopisch gelabelde componenten</li>
          <li>In situ microcosms (BACTRAP®)</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- BLOCK 2 -->
  <section class="block reverse">
    <div class="text">
      <h2>Fytoremediatie-specifieke bodem en plant-staalname</h2>
      <p class="lead">
        Volgens jarenlange ervaring bestaat er geen site-onafhankelijke strategie om biodegradatie te karakteriseren.
        De keuze van methoden hangt vooral af van het doel: bewijs voor natuurlijke attenuatie of voorbereiding van in situ
        versterking van degradatie.
      </p>
      <p class="lead">
        Ook contaminantpatronen, historiek, hydrogeologie en saneringscondities bepalen de juiste aanpak.
        We interpreteren resultaten in context van concentraties, omgevingsfactoren en hydrogeologische condities.
      </p>

      <div class="key">
        <div class="key-title">Key methods</div>
        <ul>
          <li>Plant pot assays, rapid throughput screening</li>
          <li>In situ tree cores, sap flow (phyto-forensics)</li>
        </ul>
      </div>
    </div>

    <div class="photo">
      <img src="{{ '/images/restore-2.jpg' | relative_url }}" alt="Bodem- en plantstaalname voor fytoremediatie">
    </div>
  </section>

  <!-- BLOCK 3 -->
  <section class="block">
    <div class="photo">
      <img src="{{ '/images/restore-3.jpg' | relative_url }}" alt="Monitoring van fytoremediatie en natuurlijke attenuatie">
    </div>

    <div class="text">
      <h2>Monitoring fytoremediatie en natuurlijke attenuatie</h2>
      <p class="lead">
        Een grondige analyse van biologische processen op verontreinigde sites is essentieel voor saneringsplanning.
        Wie natuurlijke attenuatie correct meeneemt, kan kosten sterk reduceren — zonder onzekerheid te creëren.
      </p>
      <p class="lead">
        In een <strong>multiple-line-of-evidence</strong> aanpak combineren we onafhankelijke methoden om conclusies te valideren
        over het degradatieproces.
      </p>

      <div class="key">
        <div class="key-title">Wat zit er in monitoring</div>
        <ul>
          <li>Success control monitoring van gestimuleerde fytoremediatie</li>
          <li>Multi-line-of-evidence: chemische analyses (CSIA, BACTRAP®, diagnostische ratio’s, metabolieten) + microbiologie</li>
          <li>Plant tissue sampling: BAF/TF berekening + aanbevelingen voor veilige verwerking/afvoer</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- CTA -->
  <section class="cta">
    <div class="cta-inner">
      <div>
        <h3>Restore-traject opstarten?</h3>
        <p>Stuur je locatie, vraag en bestaande analyses. Dan maak ik een voorstel voor staalname, evidence-plan en monitoring.</p>
      </div>
      <a href="{{ '/contact/' | relative_url }}">Contacteer mij →</a>
    </div>
  </section>

</div>
