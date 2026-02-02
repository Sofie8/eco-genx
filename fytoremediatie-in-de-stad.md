---
title: Fytoremediatie in de stad
layout: default
permalink: /fytoremediatie-in-de-stad/
nav:
  order: 7
  tooltip: Fytoremediatie in de stad
---

<style>
  /* =========================================================
     Fytoremediatie in de stad — "seed"-achtige layout
     Links: diensten (sticky)
     Rechts: content
     ========================================================= */

  main{ max-width:none !important; padding:0 !important; overflow:visible !important; }
  main > *, main .content, main article, main .page, main .post{
    max-width:none !important; padding:0 !important; margin:0 !important; overflow:visible !important;
  }

  .city{
    --max: 1200px;
    --pad: 1.25rem;
    --cream: var(--eco-cream, #f6f4ee);
    --green: var(--eco-dark, #0b3b2f);
    --green2: var(--eco-dark-2, #082a22);
    --ink: rgba(0,0,0,.86);
    --muted: rgba(0,0,0,.66);
    --line: rgba(0,0,0,.10);
    --shadow: 0 14px 36px rgba(0,0,0,.06);
    --shadow2: 0 18px 44px rgba(0,0,0,.10);
  }

  /* Hero */
  .hero{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    background: linear-gradient(180deg, rgba(11,59,47,.92), rgba(8,42,34,.92));
    color: rgba(255,255,255,.92);
    padding: 2.4rem 0 1.8rem;
  }
  .hero .inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
  }
  .eyebrow{
    font-size: .86rem;
    letter-spacing: .10em;
    text-transform: uppercase;
    opacity: .85;
    margin-bottom: .55rem;
  }
  .hero h1{
    margin:0 0 .55rem;
    font-size: 2.4rem;
    line-height: 1.08;
  }
  .hero p{
    margin:0;
    max-width: 84ch;
    opacity:.92;
    line-height:1.7;
  }

  /* Body */
  .body{
    background: var(--cream);
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    padding: 2.2rem 0 3.2rem;
    border-top: 1px solid rgba(0,0,0,.06);
  }
  .body .inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
    display:grid;
    grid-template-columns: .42fr 1fr;
    gap: 1.25rem;
    align-items:start;
  }

  /* Sidebar */
  .side{
    position: sticky;
    top: 1.25rem;
  }
  .sidecard{
    background: rgba(255,255,255,.62);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    box-shadow: var(--shadow);
    overflow:hidden;
  }
  .sidehead{
    padding: 1.05rem 1.1rem;
    border-bottom: 1px solid rgba(0,0,0,.08);
    font-weight: 900;
    letter-spacing: .10em;
    text-transform: uppercase;
    color: rgba(0,0,0,.78);
  }
  .sidelist{
    padding: .35rem .5rem .6rem;
    display:flex;
    flex-direction: column;
    gap: .35rem;
  }
  .sidelist a{
    display:block;
    padding: .7rem .85rem;
    border-radius: 14px;
    text-decoration:none;
    color: rgba(0,0,0,.82);
    border: 1px solid rgba(0,0,0,.06);
    background: rgba(255,255,255,.70);
    transition: transform .12s ease, box-shadow .12s ease;
  }
  .sidelist a:hover{
    transform: translateY(-1px);
    box-shadow: var(--shadow2);
  }
  .sidelist small{
    display:block;
    color: var(--muted);
    margin-top: .15rem;
    line-height: 1.45;
  }

  /* Content cards */
  .card{
    background: rgba(255,255,255,.62);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    box-shadow: var(--shadow);
    overflow:hidden;
  }
  .pad{ padding: 1.25rem 1.35rem; }
  .card h2{
    margin: 0 0 .6rem;
    font-size: 1.55rem;
    color: var(--ink);
  }
  .card p, .card li{
    color: rgba(0,0,0,.72);
    line-height: 1.75;
  }
  .card ul{ margin:.6rem 0 0; padding-left: 1.1rem; }
  .card li{ margin:.35rem 0; }

  .media{
    width:100%;
    height: 280px;
    overflow:hidden;
    background: rgba(0,0,0,.06);
  }
  .media img{
    width:100%;
    height:100%;
    object-fit: cover;
    display:block;
  }

  .cta{
    margin-top: 1.1rem;
    background: rgba(11,59,47,.92);
    color: rgba(255,255,255,.92);
    border: 1px solid rgba(255,255,255,.12);
    border-radius: 18px;
    padding: 1.1rem 1.2rem;
  }
  .cta a{
    color: rgba(255,255,255,.92);
    text-decoration:none;
    border-bottom: 1px solid rgba(255,255,255,.35);
    padding-bottom: .08rem;
    font-weight: 800;
  }

  @media (max-width: 980px){
    .body .inner{ grid-template-columns: 1fr; }
    .side{ position: static; }
    .media{ height: 240px; }
    .hero h1{ font-size: 2.05rem; }
  }
</style>

<div class="city">

  <section class="hero">
    <div class="inner">
      <div class="eyebrow">Eco-GenX · Fytoremediatie in de stad</div>
      <h1>Van stedelijke bodem naar werkend groen</h1>
      <p>
        Praktische trajecten rond plantkeuze, inventarisatie en monitoring — met aandacht voor eco-regio, stressfactoren
        en “meetbaar bewijs” op terrein.
      </p>
    </div>
  </section>

  <section class="body">
    <div class="inner">

      <!-- LEFT: diensten -->
      <aside class="side" aria-label="Diensten">
        <div class="sidecard">
          <div class="sidehead">Diensten</div>
          <div class="sidelist">
            <a href="#inventarisatie">
              Terrein-toets: planten & kruiden
              <small>Inventarisatie, habitat, indicatiewaarden, quick wins.</small>
            </a>
            <a href="#ecoregio">
              Eco-regio & standplaatsanalyse
              <small>Wat kan hier echt werken — bodem, water, stress, beheer.</small>
            </a>
            <a href="#klimaatboom">
              Klimaatboom labelling
              <small>Robuustheid, risico’s, beheeradvies en communicatie naar burgers.</small>
            </a>
            <a href="#contact">
              Traject op maat
              <small>Van diagnose naar ontwerp & monitoringplan.</small>
            </a>
          </div>
        </div>
      </aside>

      <!-- RIGHT: content -->
      <div>

        <div class="card">
          <div class="media">
            <img src="{{ '/images/fyto-stad-hero.jpg' | relative_url }}" alt="Fytoremediatie in de stad">
          </div>
          <div class="pad">
            <h2>Waarom fytoremediatie in stedelijke context?</h2>
            <p>
              Stadsbodems zijn complex: verdichting, droogte, hitte, fragmentatie en soms verontreiniging.
              Daarom combineer ik ecologie + plantkeuze + monitoring zodat je niet “gokt”, maar gericht bijstuurt.
            </p>
          </div>
        </div>

        <div class="card" id="inventarisatie" style="margin-top:1.1rem;">
          <div class="pad">
            <h2>Terrein-toets: planten & kruiden inventarisatie</h2>
            <ul>
              <li>inventarisatie (soorten, bedekking, indicatorsoorten)</li>
              <li>stress-signalen en beheerknelpunten</li>
              <li>kansenkaart: snelle ingrepen vs. langere trajecten</li>
            </ul>
          </div>
        </div>

        <div class="card" id="ecoregio" style="margin-top:1.1rem;">
          <div class="pad">
            <h2>Eco-regio & standplaatsanalyse</h2>
            <ul>
              <li>eco-regio/standplaats match: water, textuur, organische stof</li>
              <li>risico’s: droogte/hitte, zout, verdichting</li>
              <li>keuze van soorten/rassen + beheeradvies</li>
            </ul>
          </div>
        </div>

        <div class="card" id="klimaatboom" style="margin-top:1.1rem;">
          <div class="pad">
            <h2>Klimaatboom labelling</h2>
            <ul>
              <li>labeling voor robuustheid & beheer (duidelijk naar burgers)</li>
              <li>monitoringkader: KPI’s, signalen, bijsturing</li>
              <li>communicatie: “waarom deze boom hier?”</li>
            </ul>
          </div>
        </div>

        <div class="cta" id="contact">
          Wil je dit toepassen op jouw wijk/park/straat? <a href="{{ '/contact/' | relative_url }}">Contacteer mij →</a>
        </div>

      </div>

    </div>
  </section>

</div>
