---
title: Fytoremediatie in de stad
layout: default
permalink: /fytoremediatie-in-de-stad/
nav:
  order: 6
  tooltip: Fytoremediatie in de stad
---

<style>
  /* =========================================================
     Fytoremediatie in de stad — 2-col intro + split sections
     (geen kaders, wél full-width, zoals missie/visie)
     Scoped: .city
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
  }

  /* full-bleed helpers */
  .city .bleed{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw;
    margin-right: -50vw;
  }
  .city .inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
  }

  /* ---------- HERO (klein, zoals artikels) ---------- */
  .city-hero{
    background: linear-gradient(180deg, rgba(11,59,47,.92), rgba(8,42,34,.92));
    color: rgba(255,255,255,.92);
    padding: 2.2rem 0 1.6rem;
    border-bottom: 1px solid rgba(0,0,0,.10);
  }
  .city-hero .eyebrow{
    font-size: .86rem;
    letter-spacing: .10em;
    text-transform: uppercase;
    opacity: .85;
    margin-bottom: .55rem;
  }
  .city-hero h1{
    margin:0 0 .55rem;
    font-size: 2.35rem;
    line-height: 1.08;
    text-align:left;
  }
  .city-hero p{
    margin:0;
    max-width: 90ch;
    opacity:.92;
    line-height:1.7;
    text-align:left;
  }

  /* ---------- SECTION BASE ---------- */
  .sec{
    background: var(--cream);
    padding: 2.4rem 0;
    border-top: 1px solid rgba(0,0,0,.06);
  }

  /* 2 kolommen intro (geen kader) */
  .two-col{
    display:grid;
    grid-template-columns: 1fr 1fr;
    gap: 2.2rem;
    align-items: start;
  }
  .two-col h2{
    margin: 0;
    font-size: 2.1rem;
    line-height: 1.12;
    letter-spacing: .01em;
    color: var(--ink);
    text-align:left;
  }
  .two-col .txt p{
    margin: 0;
    color: rgba(0,0,0,.74);
    line-height: 1.85;
    font-size: 1.05rem;
    text-align:left;
  }
  .two-col .txt p + p{ margin-top: .9rem; }

  /* Split blok: links content, rechts foto (full cover) */
  .split{
    display:grid;
    grid-template-columns: .95fr 1.05fr;
    gap: 2rem;
    align-items: stretch;
  }

  /* Links: lijst/inhoud */
  .split-left h2{
    margin: 0 0 .75rem;
    font-size: 1.75rem;
    line-height: 1.2;
    color: var(--ink);
    text-align:left;
  }
  .split-left p{
    margin: 0 0 1.05rem;
    color: rgba(0,0,0,.74);
    line-height: 1.85;
    text-align:left;
    max-width: 80ch;
  }

  /* “diensten” lijst als nette blokken, geen card look */
  .svc{
    display:flex;
    flex-direction: column;
    gap: .9rem;
    margin-top: .2rem;
  }
  .svc a{
    display:block;
    text-decoration:none;
    color: inherit;
    padding: .9rem 1rem;
    border: 1px solid rgba(0,0,0,.10);
    background: rgba(255,255,255,.55);
    border-radius: 16px;
  }
  .svc a strong{
    display:block;
    font-size: 1.05rem;
    margin-bottom: .2rem;
  }
  .svc a span{
    display:block;
    color: rgba(0,0,0,.66);
    line-height: 1.65;
  }
  .svc a:hover{
    background: rgba(255,255,255,.70);
  }

  /* Foto rechts / links: altijd gelijk, cover */
  .split-media{
    border-radius: 18px;
    overflow:hidden;
    border: 1px solid rgba(0,0,0,.10);
    background: rgba(0,0,0,.06);
    min-height: 420px;
  }
  .split-media img{
    width:100%;
    height:100%;
    object-fit: cover;
    display:block;
  }

  /* Aanpak bullets */
  .bul{
    margin: .35rem 0 0;
    padding-left: 1.1rem;
  }
  .bul li{
    margin: .45rem 0;
    color: rgba(0,0,0,.74);
    line-height: 1.85;
    text-align:left;
  }

  /* CTA */
  .cta{
    margin-top: 1.5rem;
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

  /* Responsive */
  @media (max-width: 980px){
    .two-col{ grid-template-columns: 1fr; gap: 1.2rem; }
    .two-col h2{ font-size: 1.85rem; }
    .split{ grid-template-columns: 1fr; }
    .split-media{ min-height: 280px; }
  }
</style>

<div class="city">

  <!-- HERO -->
  <section class="bleed city-hero" aria-label="Fytoremediatie in de stad">
    <div class="inner">
      <div class="eyebrow">Eco-GenX · Fytoremediatie in de stad</div>
      <h1>Van stedelijke bodem naar werkend groen</h1>
      <p>
        Praktische trajecten rond plantkeuze, inventarisatie en monitoring — met aandacht voor eco-regio,
        stressfactoren en meetbaar bewijs op terrein.
      </p>
    </div>
  </section>

  <!-- INTRO: 2 kolommen, geen kader -->
  <section class="bleed sec" aria-label="Waarom fytoremediatie in stedelijke context">
    <div class="inner">
      <div class="two-col">
        <h2>Waarom fytoremediatie in stedelijke context?</h2>
        <div class="txt">
          <p>
            Stadsbodems zijn complex: verdichting, droogte, hitte, fragmentatie en soms verontreiniging.
            Daarom combineer ik ecologie + plantkeuze + monitoring zodat je niet “gokt”, maar gericht bijstuurt.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- DIENSTEN links, FOTO rechts (full cover) -->
  <section class="bleed sec" aria-label="Diensten en aanpak">
    <div class="inner">
      <div class="split">

        <div class="split-left">
          <h2>Diensten</h2>
          <p>
            Los inzetbaar of als traject: van snelle terrein-toets tot onderbouwd beheeradvies en monitoringkader.
          </p>

          <div class="svc">
            <a href="#inventarisatie">
              <strong>Terrein-toets: planten & kruiden inventarisatie</strong>
              <span>Inventarisatie, indicatorsoorten, stress-signalen en quick wins.</span>
            </a>

            <a href="#ecoregio">
              <strong>Eco-regio & standplaatsanalyse</strong>
              <span>Water/bodem match, risico’s (droogte/hitte/zout/verdichting) en soortenkeuze.</span>
            </a>

            <a href="#klimaatboom">
              <strong>Klimaatboom labelling</strong>
              <span>Robuustheid, beheer, KPI’s en communicatie: “waarom deze boom hier?”.</span>
            </a>

            <a href="#contact">
              <strong>Traject op maat</strong>
              <span>Van diagnose naar ontwerp, proefopzet en monitoringplan.</span>
            </a>
          </div>
        </div>

        <div class="split-media" aria-label="Beeld stedelijk groen">
          <img src="{{ '/images/fyto-stad-1.jpg' | relative_url }}" alt="Stedelijke fytoremediatie">
        </div>

      </div>
    </div>
  </section>

  <!-- ECO-GENX AANPAK: FOTO links, BULLETS rechts -->
  <section class="bleed sec" aria-label="Eco-GenX aanpak">
    <div class="inner">
      <div class="split">

        <div class="split-media" aria-label="Beeld terrein en monitoring">
          <img src="{{ '/images/fyto-stad-2.jpg' | relative_url }}" alt="Terrein-toets en monitoring">
        </div>

        <div class="split-left">
          <h2>Eco-GenX aanpak</h2>
          <p>
            Eenvoudig, meetbaar en iteratief: <strong>meten → begrijpen → bijsturen</strong>.
            Dit is wat het traject omvat:
          </p>

          <div id="inventarisatie">
            <p><strong>Terrein-toets: planten & kruiden inventarisatie</strong></p>
            <ul class="bul">
              <li>inventarisatie (soorten, bedekking, indicatorsoorten)</li>
              <li>stress-signalen en beheerknelpunten</li>
              <li>kansenkaart: snelle ingrepen vs. langere trajecten</li>
            </ul>
          </div>

          <div id="ecoregio" style="margin-top:1rem;">
            <p><strong>Eco-regio & standplaatsanalyse</strong></p>
            <ul class="bul">
              <li>eco-regio/standplaats match: water, textuur, organische stof</li>
              <li>risico’s: droogte/hitte, zout, verdichting</li>
              <li>keuze van soorten/rassen + beheeradvies</li>
            </ul>
          </div>

          <div id="klimaatboom" style="margin-top:1rem;">
            <p><strong>Klimaatboom labelling</strong></p>
            <ul class="bul">
              <li>labeling voor robuustheid & beheer (duidelijk naar burgers)</li>
              <li>monitoringkader: KPI’s, signalen, bijsturing</li>
              <li>communicatie: “waarom deze boom hier?”</li>
            </ul>
          </div>

          <div class="cta" id="contact">
            Wil je dit toepassen op jouw wijk/park/straat? <a href="{{ '/contact/' | relative_url }}">Contacteer mij →</a>
          </div>

        </div>

      </div>
    </div>
  </section>

</div>
