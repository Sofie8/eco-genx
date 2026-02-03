---
title: Voor wie
layout: default
permalink: /over/voor-wie/
---

<style>
  /* =========================================================
     Voor wie — split layout (image left, content right)
     Scope: .vw
     ========================================================= */

  /* full width page */
  main{ max-width:none !important; padding:0 !important; overflow:visible !important; }
  main > *, main .content, main article, main .page, main .post{
    max-width:none !important; padding:0 !important; margin:0 !important; overflow:visible !important;
  }

  /* hide default h1 that layout might inject */
  .page-title,
  .page-header,
  .page-header h1,
  h1.page-title,
  main > h1:first-child{
    display:none !important;
  }

  .vw{
    --max: 1200px;
    --pad: 1.25rem;
    --cream: var(--eco-cream, #f6f4ee);
    --ink: rgba(0,0,0,.86);
    --muted: rgba(0,0,0,.66);
    --line: rgba(0,0,0,.10);
    --green: var(--eco-dark, #0b3b2f);
    --green2: var(--eco-dark-2, #082a22);
  }

  /* header band (like your other pages) */
  .vw-hero{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    background: linear-gradient(180deg, rgba(11,59,47,.92), rgba(8,42,34,.92));
    color: rgba(255,255,255,.92);
    padding: 3.0rem 0 1.8rem;
  }
  .vw-hero .inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
  }
  .vw-eyebrow{
    font-size: .86rem;
    letter-spacing: .10em;
    text-transform: uppercase;
    opacity: .82;
    margin: 0 0 .6rem;
  }
  .vw-hero h1{
    margin: 0 0 .5rem;
    font-size: 2.6rem;
    line-height: 1.06;
    letter-spacing: .02em;
  }
  .vw-hero p{
    margin: 0;
    max-width: 80ch;
    opacity: .92;
    line-height: 1.7;
    font-size: 1.05rem;
  }

  /* split section */
  .vw-body{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    background: var(--cream);
    border-top: 1px solid rgba(0,0,0,.06);
    padding: 2.2rem 0 3.0rem;
  }
  .vw-body .inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);

    display: grid;
    grid-template-columns: .95fr 1.05fr; /* left image a bit smaller */
    gap: 1.6rem;
    align-items: start;
  }

  /* left image card */
  .vw-photo{
    border-radius: 20px;
    overflow: hidden;
    border: 1px solid rgba(0,0,0,.08);
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
    background: rgba(255,255,255,.55);

    position: sticky;
    top: 1.25rem;
  }
  .vw-photo .frame{
    aspect-ratio: 4 / 5; /* nice vertical like your example */
    background: rgba(0,0,0,.06);
  }
  .vw-photo img{
    width: 100%;
    height: 100%;
    object-fit: cover; /* always clean crop, no scrollbars */
    display: block;
  }
  .vw-photo .cap{
    padding: .95rem 1.0rem;
    color: var(--muted);
    line-height: 1.65;
    border-top: 1px solid rgba(0,0,0,.06);
  }

  /* right content card */
  .vw-card{
    background: rgba(255,255,255,.65);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 20px;
    padding: 1.5rem 1.6rem;
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
  }

  .vw-card h2{
    margin: 0 0 .65rem;
    font-size: 1.7rem;
    line-height: 1.15;
    color: var(--ink);
  }
  .vw-card p{
    margin: 0 0 1rem;
    color: var(--muted);
    line-height: 1.75;
  }

  .vw-grid{
    display:grid;
    grid-template-columns: repeat(2, minmax(0,1fr));
    gap: 1rem;
    margin-top: 1rem;
  }
  .vw-mini{
    border: 1px solid rgba(0,0,0,.08);
    background: rgba(255,255,255,.55);
    border-radius: 16px;
    padding: 1rem 1rem;
  }
  .vw-mini h3{
    margin: 0 0 .35rem;
    font-size: 1.05rem;
    color: var(--ink);
  }
  .vw-mini ul{
    margin: .4rem 0 0;
    padding-left: 1.1rem;
    color: rgba(0,0,0,.74);
    line-height: 1.7;
  }
  .vw-mini li{ margin: .3rem 0; }

  .vw-cta{
    margin-top: 1.2rem;
    padding-top: 1.2rem;
    border-top: 1px solid rgba(0,0,0,.08);
    display:flex;
    flex-wrap:wrap;
    gap:.7rem;
    align-items:center;
    justify-content: space-between;
  }
  .vw-cta a{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    padding: .7rem 1rem;
    border-radius: 12px;
    text-decoration:none;
    border: 1px solid rgba(11,59,47,.25);
    color: rgba(11,59,47,.92);
    background: rgba(11,59,47,.06);
  }
  .vw-cta a:hover{ background: rgba(11,59,47,.10); }

  @media (max-width: 980px){
    .vw-hero h1{ font-size: 2.1rem; }
    .vw-body .inner{ grid-template-columns: 1fr; }
    .vw-photo{ position: static; }
    .vw-photo .frame{ aspect-ratio: 16 / 10; }
    .vw-grid{ grid-template-columns: 1fr; }
  }
</style>

<div class="vw">

  <!-- top band -->
  <section class="vw-hero">
    <div class="inner">
      <div class="vw-eyebrow">Over Eco-GenX</div>
      <h1>Voor wie</h1>
      <p>
        Eco-GenX werkt voor organisaties die natuur en ondergrond ernstig nemen: van analyse tot implementatie,
        met meetbaar bewijs en heldere keuzes.
      </p>
    </div>
  </section>

  <!-- split -->
  <section class="vw-body">
    <div class="inner">

      <!-- LEFT: image -->
      <aside class="vw-photo" aria-label="Sfeerbeeld">
        <div class="frame">
          <img src="{{ '/images/voor-wie.jpg' | relative_url }}" alt="Eco-GenX — veldwerk en interpretatie">
        </div>
        <div class="cap">
          Voeg hier één beeld toe dat je verhaal draagt (veldwerk, bodemprofiel, monitoring, labo…).
          Bestandsnaam: <code>images/voor-wie.jpg</code>.
        </div>
      </aside>

      <!-- RIGHT: your text (replace with your current content) -->
      <article class="vw-card">
        <h2>Decision-ready advies voor…</h2>
        <p>
          <!-- plak hier je bestaande “voor wie” intro-tekst -->
          Ingenieursbureaus, overheden, terreinbeheerders, bedrijven en burgerinitiatieven die een
          bodem-/watervraagstuk willen oplossen met een aanpak die technisch klopt én praktisch werkt.
        </p>

        <div class="vw-grid">
          <div class="vw-mini">
            <h3>Overheden & publieke partners</h3>
            <ul>
              <li>strategie en prioritering</li>
              <li>monitoring & interpretatie</li>
              <li>duiding voor communicatie</li>
            </ul>
          </div>

          <div class="vw-mini">
            <h3>Ingenieursbureaus & aannemers</h3>
            <ul>
              <li>evidence-plan / KPI’s</li>
              <li>proefopzet & evaluatie</li>
              <li>veld → rapport → keuze</li>
            </ul>
          </div>

          <div class="vw-mini">
            <h3>Bedrijven & sites</h3>
            <ul>
              <li>haalbaarheidsinschatting</li>
              <li>risk-based keuzes</li>
              <li>verificatie van maatregelen</li>
            </ul>
          </div>

          <div class="vw-mini">
            <h3>Burgers & verenigingen</h3>
            <ul>
              <li>lezingen / Q&A</li>
              <li>interpretatie van meetdata</li>
              <li>praktische handvaten</li>
            </ul>
          </div>
        </div>

        <div class="vw-cta">
          <div style="color: rgba(0,0,0,.66); line-height:1.6;">
            Twijfel je of jouw case past? Stuur 5 regels + locatie + wat je al gemeten hebt.
          </div>
          <a href="{{ '/contact/' | relative_url }}">Contacteer mij →</a>
        </div>
      </article>

    </div>
  </section>

</div>

