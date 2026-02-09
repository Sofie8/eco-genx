---
title: Certificaten
layout: default
permalink: /certificaten/
nav:
  order: 7
  tooltip: Certificaten
---

<style>
  /* =========================================================
     Certificaten — 2x2 grid zoals je screenshot (full width)
     Scoped to .cert-wrap
     ========================================================= */

  /* maak deze pagina full width (geen witte band/padding van main) */
  main{ max-width:none !important; padding:0 !important; overflow:visible !important; }
  main > *, main .content, main article, main .page, main .post{
    max-width:none !important; padding:0 !important; margin:0 !important; overflow:visible !important;
  }

  .cert-wrap{
    --max: 1200px;
    --pad: 1.25rem;

    --cream: var(--eco-cream, #f6f4ee);
    --green: var(--eco-dark, #0b3b2f);
    --green2: var(--eco-dark-2, #082a22);

    --ink: rgba(0,0,0,.86);
    --muted: rgba(0,0,0,.68);
    --line: rgba(0,0,0,.08);
    --accent: var(--eco-accent, #4bbf7a);
  }

  /* 2x2 grid container */
  .cert-grid{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw;
    margin-right: -50vw;

    display:grid;
    grid-template-columns: 1fr 1fr;
    grid-auto-rows: minmax(420px, auto);
    background: #fff;
  }

  .cell{
    min-height: 420px;
    border-bottom: 1px solid var(--line);
  }

  /* images */
  .cell.photo{
    position: relative;
    overflow: hidden;
    background: #111;
  }
  .cell.photo img{
    width:100%;
    height:100%;
    object-fit: cover;
    display:block;
  }

  /* text cells */
  .cell.text{
    background: #fff;
    padding: 3.2rem 3rem;
    display:flex;
    flex-direction:column;
    justify-content:center;
    gap: 1rem;
  }

  .kicker{
    font-size: .88rem;
    letter-spacing: .10em;
    text-transform: uppercase;
    color: rgba(11,59,47,.78);
    margin:0;
  }

  .cell.text h2{
    margin: 0;
    font-size: 1.9rem;
    line-height: 1.12;
    color: var(--ink);
  }

  .cell.text p{
    margin: 0;
    color: var(--muted);
    line-height: 1.75;
    max-width: 78ch;
  }

  .cell.text strong{
    color: rgba(11,59,47,.95);
  }

  .cert-links{
    margin-top: .4rem;
    display:flex;
    flex-wrap:wrap;
    gap: .75rem;
  }
  .cert-links a{
    text-decoration:none;
    color: rgba(11,59,47,.95);
    font-weight: 650;
    border-bottom: 1px solid rgba(11,59,47,.28);
    padding-bottom: .08rem;
  }
  .cert-links a:hover{
    border-bottom-color: rgba(11,59,47,.55);
  }

  /* optional small logo area */
  .badge-row{
    margin-top: .6rem;
    display:flex;
    gap: 1rem;
    align-items:center;
  }
  .badge-row img{
    height: 46px;
    width: auto;
    display:block;
  }

  /* Responsive */
  @media (max-width: 980px){
    .cert-grid{
      grid-template-columns: 1fr;
      grid-auto-rows: auto;
    }
    .cell.photo{ min-height: 320px; }
    .cell.text{ padding: 2.2rem 1.25rem; }
    .cell.text h2{ font-size: 1.65rem; }
  }
</style>

<div class="cert-wrap">

  <section class="cert-grid">

    <!-- TOP-LEFT: TEXT -->
    <div class="cell text">
      <p class="kicker"> Gecertificeerde kwaliteitsaanpak </p>
      <h2>Een gecertificeerde kwaliteitsaanpak</h2>

      <p>
        Voor projecten waar <strong>meetbaar bewijs</strong> telt, is kwaliteit geen detail maar een voorwaarde.
        Eco-GenX werkt met gevalideerde methoden, traceerbare workflows en heldere rapportering —
        zodat je beslissingen kan nemen met vertrouwen.
      </p>

      <p>
        Waar relevant sluiten we aan op <strong>ISO 17025-principes</strong> (kwaliteit & competentie in laboratoria),
        inter-laboratorium vergelijkingen en robuuste documentatie van staalname tot interpretatie.
      </p>

      <!-- optioneel: zet hier een logo als je wil -->
      <!--
      <div class="badge-row">
        <img src="{{ '/images/cofrac.png' | relative_url }}" alt="Accreditatie / certificatie logo">
      </div>
      -->

      <div class="cert-links">
        <a href="{{ '/contact/' | relative_url }}">Vraag certificatie-info →</a>
        <a href="{{ '/projects/' | relative_url }}">Bekijk projecten →</a>
      </div>
    </div>

    <!-- TOP-RIGHT: PHOTO -->
    <div class="cell photo">
      <img src="{{ '/images/cert-1.jpg' | relative_url }}" alt="Gecertificeerde kwaliteitsaanpak">
    </div>

    <!-- BOTTOM-LEFT: TEXT -->
    <div class="cell text">
      <p class="kicker">Analytische expertise</p>
      <h2>Van analyse naar decision-ready conclusies</h2>

      <p>
        Certificatie is pas waardevol als het ook leidt tot betere beslissingen.
        Daarom koppelen we meetdata aan context: veldcondities, historiek, hydrogeologie en risico’s.
        Je krijgt niet enkel resultaten, maar ook <strong>interpretatie</strong> en <strong>actiepunten</strong>.
      </p>

      <p>
        Denk aan: kwaliteitscontrole op stalen, methodeselectie per doel (bewijs natuurlijke attenuatie,
        monitoring, interventie-validatie) en transparante rapportering die je intern én extern kan verantwoorden.
      </p>

      <div class="cert-links">
        <a href="{{ '/contact/' | relative_url }}">Even sparren →</a>
        <a href="{{ '/over/onderzoek/' | relative_url }}">Onderzoek & methodes →</a>
      </div>
    </div>

    <!-- BOTTOM-RIGHT: PHOTO -->
    <div class="cell photo">
      <img src="{{ '/images/cert-2.jpg' | relative_url }}" alt="Analytische expertise en labo/veld workflow">
    </div>

  </section>

</div>
