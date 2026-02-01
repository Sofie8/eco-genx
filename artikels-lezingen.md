---
title: Artikels & lezingen
layout: default
permalink: /over/artikels-lezingen/
nav:
  order: 3
  tooltip: Artikels & lezingen
---

<style>
  /* =========================================================
     Artikels & Lezingen — Eco-GenX style (zoals projecten)
     - full-bleed header (niet te hoog)
     - 2-kolom cards (lezingen met agenda)
     ========================================================= */

  /* full width page */
  main{ max-width:none !important; padding:0 !important; overflow:visible !important; }
  main > *, main .content, main article, main .page, main .post{
    max-width:none !important; padding:0 !important; margin:0 !important; overflow:visible !important;
  }

  .al{
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

  /* Header hero (full-bleed, beperkte hoogte) */
  .al-hero{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    background-image: url("{{ '/images/artikels-lezingen-hero.jpg' | relative_url }}");
    background-size: cover;
    background-position: center;
    min-height: 240px;        /* ✅ niet zo hoog */
  }
  .al-hero::before{
    content:"";
    position:absolute; inset:0;
    background: linear-gradient(90deg,
      rgba(8,42,34,.84) 0%,
      rgba(8,42,34,.58) 44%,
      rgba(8,42,34,.20) 100%);
  }
  .al-hero__inner{
    position: relative;
    max-width: var(--max);
    margin: 0 auto;
    padding: 2.2rem var(--pad);
    color: rgba(255,255,255,.92);
  }
  .al-eyebrow{
    font-size: .86rem;
    letter-spacing: .10em;
    text-transform: uppercase;
    opacity: .88;
    margin-bottom: .55rem;
  }
  .al-hero h1{
    margin: 0 0 .45rem;
    font-size: 2.4rem;
    line-height: 1.08;
    letter-spacing: .02em;
  }
  .al-hero p{
    margin: 0;
    max-width: 78ch;
    opacity: .92;
    line-height: 1.7;
  }

  /* Content area */
  .al-body{
    background: var(--cream);
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    padding: 2.2rem 0 3.2rem;
    border-top: 1px solid rgba(0,0,0,.06);
  }
  .al-body__inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
  }

  .al-section{
    margin: 0 0 2.2rem;
  }
  .al-section h2{
    margin: 0 0 .75rem;
    font-size: 1.55rem;
    color: var(--ink);
  }

  /* 2-col layout */
  .al-grid{
    display:grid;
    grid-template-columns: 1.15fr .85fr;
    gap: 1.25rem;
    align-items: start;
  }

  /* Cards */
  .al-card{
    background: rgba(255,255,255,.60);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    box-shadow: var(--shadow);
    overflow:hidden;
  }
  .al-card__pad{
    padding: 1.35rem 1.45rem;
  }
  .al-card h3{
    margin: 0 0 .55rem;
    font-size: 1.35rem;
    color: var(--ink);
  }
  .al-card p{
    margin: 0 0 .85rem;
    color: var(--muted);
    line-height: 1.75;
  }
  .al-card ul{
    margin: .6rem 0 0;
    padding-left: 1.1rem;
    color: rgba(0,0,0,.74);
  }
  .al-card li{ margin: .35rem 0; }

  /* Agenda */
  .agenda-head{
    display:flex;
    align-items: baseline;
    justify-content: space-between;
    gap: 1rem;
    padding: 1.15rem 1.25rem .85rem;
    border-bottom: 1px solid rgba(0,0,0,.08);
  }
  .agenda-head strong{
    letter-spacing: .10em;
    text-transform: uppercase;
    font-size: .95rem;
    color: var(--ink);
  }
  .agenda-head span{
    color: var(--muted);
  }

  .agenda{
    padding: 1rem 1.1rem 1.2rem;
    display:flex;
    flex-direction: column;
    gap: .9rem;
  }
  .ag-item{
    display:grid;
    grid-template-columns: 9.5rem 1fr;
    gap: 1rem;
    padding: .95rem 1rem;
    border-radius: 16px;
    background: rgba(255,255,255,.72);
    border: 1px solid rgba(0,0,0,.08);
  }
  .ag-date{
    font-weight: 800;
    font-size: 1.05rem;
    color: rgba(0,0,0,.82);
    line-height: 1.15;
    letter-spacing: .02em;
    white-space: nowrap;
  }
  .ag-main{
    display:flex;
    flex-direction: column;
    gap: .15rem;
    min-width: 0;
  }
  .ag-title{
    font-weight: 700;
    color: var(--ink);
    line-height: 1.25;
  }
  .ag-meta{
    color: var(--muted);
    line-height: 1.5;
    font-size: .98rem;
  }
  .ag-link{
    margin-top: .25rem;
    align-self: flex-start;
    text-decoration: none;
    font-weight: 700;
    color: rgba(11,59,47,.92);
    border-bottom: 1px solid rgba(11,59,47,.35);
    padding-bottom: .06rem;
  }

  /* Article blocks */
  .article{
    display:grid;
    grid-template-columns: 1fr;
    gap: .6rem;
    padding: 1.1rem 1.2rem;
    border-top: 1px solid rgba(0,0,0,.08);
  }
  .article:first-child{ border-top: 0; }
  .article strong{ color: var(--ink); }
  .article .meta{ color: var(--muted); }
  .article a{
    text-decoration:none;
    font-weight:700;
    color: rgba(11,59,47,.92);
    border-bottom: 1px solid rgba(11,59,47,.35);
    padding-bottom: .06rem;
    align-self: flex-start;
  }

  /* Inline image (code of good practice) */
  .imgbox{
    background: rgba(255,255,255,.72);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    overflow:hidden;
    box-shadow: var(--shadow);
  }
  .imgbox img{
    width:100%;
    height:auto;
    display:block;
  }
  .imgcap{
    padding: .85rem 1rem;
    color: var(--muted);
    line-height: 1.6;
  }

  @media (max-width: 980px){
    .al-hero{ min-height: 210px; }
    .al-hero__inner{ padding: 1.7rem var(--pad); }
    .al-hero h1{ font-size: 2.0rem; }
    .al-grid{ grid-template-columns: 1fr; }
    .ag-item{ grid-template-columns: 1fr; }
    .ag-date{ white-space: normal; }
  }
</style>

<div class="al">

  <!-- HEADER -->
  <section class="al-hero">
    <div class="al-hero__inner">
      <div class="al-eyebrow">Eco-GenX · Artikels & lezingen</div>
      <h1>Maak kennis met Sofie (Eco-GenX)</h1>
      <p>Op één van volgende momenten — of boekbaar op aanvraag voor burgers, gemeenten en verenigingen.</p>
    </div>
  </section>

  <section class="al-body">
    <div class="al-body__inner">

      <!-- 1) LEZINGEN -->
      <div class="al-section" id="lezingen">
        <div class="al-grid">

          <!-- Left: text -->
          <div class="al-card">
            <div class="al-card__pad">
              <h3>Lezingen & sessies voor burgers</h3>
              <p>
                Ik geef lezingen en Q&amp;A’s (bv. PFAS/bodem/water, nature-based oplossingen, monitoring en interpretatie).
                Altijd met ruimte voor vragen en vertaald naar “wat betekent dit concreet?”.
              </p>
              <ul>
                <li>uitleg zonder jargon, met correcte nuance</li>
                <li>praktische handvaten voor vragen en beslissingen</li>
                <li>duiding van meetdata en onzekerheden</li>
              </ul>
            </div>
          </div>

          <!-- Right: agenda -->
          <div class="al-card" aria-label="Agenda lezingen">
            <div class="agenda-head">
              <strong>Agenda</strong>
              <span>pas aan / voeg regels toe</span>
            </div>

            <div class="agenda">

              <!-- ✅ COPY/PASTE dit blok om extra events toe te voegen -->
              <div class="ag-item">
                <div class="ag-date">12 feb 2026</div>
                <div class="ag-main">
                  <div class="ag-title">Lezing Ekeren</div>
                  <div class="ag-meta">19:30 · Ekeren · PFAS &amp; meetdata — interpretatie en vragen</div>
                  <a class="ag-link" href="{{ '/contact/' | relative_url }}">Info / inschrijven →</a>
                </div>
              </div>

              <div class="ag-item">
                <div class="ag-date">28 mrt 2026</div>
                <div class="ag-main">
                  <div class="ag-title">Lezing Ronse</div>
                  <div class="ag-meta">20:00 · Ronse · Bodem &amp; water — nature-based opties</div>
                  <a class="ag-link" href="{{ '/contact/' | relative_url }}">Info / inschrijven →</a>
                </div>
              </div>

              <div class="ag-item">
                <div class="ag-date">—</div>
                <div class="ag-main">
                  <div class="ag-title">Boekbaar op aanvraag</div>
                  <div class="ag-meta">Gemeenten, burgergroepen, verenigingen · onderwerp op maat</div>
                  <a class="ag-link" href="{{ '/contact/' | relative_url }}">Vraag een lezing aan →</a>
                </div>
              </div>

            </div>
          </div>

        </div>
      </div>

      <!-- 2) ARTIKELS -->
      <div class="al-section" id="artikels">
        <h2>Artikels & publicaties</h2>

        <div class="al-grid">

          <!-- Left: articles list -->
          <div class="al-card">
            <div class="al-card__pad">
              <h3>Overzicht</h3>
              <p>Korte links naar artikels, posts of documenten. Voeg toe wanneer je wil.</p>
            </div>

            <!-- Article items -->
            <div class="article">
              <strong>Code van goede praktijk (OVAM)</strong>
              <div class="meta">Praktische richtlijnen &amp; aanpak — PDF / beeld hieronder</div>
              <a href="{{ '/contact/' | relative_url }}">Link toevoegen →</a>
            </div>

            <div class="article">
              <strong>Artikel / blogpost (placeholder)</strong>
              <div class="meta">Datum · medium · korte omschrijving</div>
              <a href="{{ '/contact/' | relative_url }}">Link toevoegen →</a>
            </div>

            <div class="article">
              <strong>Lezingmateriaal / samenvatting (placeholder)</strong>
              <div class="meta">Slide deck / notitie / download</div>
              <a href="{{ '/contact/' | relative_url }}">Link toevoegen →</a>
            </div>

          </div>

          <!-- Right: image upload area (code of good practice) -->
          <div class="imgbox">
            <!-- ✅ Upload je afbeelding naar /images/ en pas de naam hieronder aan -->
            <img src="{{ '/images/code-van-goede-praktijk.jpg' | relative_url }}" alt="Code van goede praktijk (OVAM)">

            <div class="imgcap">
              <strong>Code van goede praktijk (OVAM)</strong><br>
              Upload een screenshot/scan als <code>/images/code-van-goede-praktijk.jpg</code>
              (of wijzig de bestandsnaam hierboven).
            </div>
          </div>

        </div>
      </div>

    </div>
  </section>

</div>
