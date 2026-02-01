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
     Artikels & lezingen — Eco-GenX (Ossiado-ish)
     - Full-bleed hero image (niet te hoog)
     - Content max-width zoals Projects
     - Cards op eco-cream
     ========================================================= */

  /* full width page (zoals services/projects) */
  main{ max-width:none !important; padding:0 !important; overflow:visible !important; }
  main > *, main .content, main article, main .page, main .post{
    max-width:none !important; padding:0 !important; margin:0 !important; overflow:visible !important;
  }

  /* Hide eventuele default titel van theme */
  .page-title,
  .page-header,
  .page-header h1,
  h1.page-title,
  main > h1:first-child{
    display:none !important;
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
  }

  /* ---------- HERO (full-bleed, niet te hoog) ---------- */
  .al-hero{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    background: var(--green2);
    border-bottom: 1px solid rgba(0,0,0,.08);
    overflow:hidden;
  }

  .al-hero__media{
    height: clamp(220px, 32vh, 340px); /* ✅ minder hoog (vertikaal) */
    min-height: 210px;
    position: relative;
  }

  .al-hero__media img{
    width:100%;
    height:100%;
    object-fit: cover;
    display:block;
  }

  .al-hero__shade{
    position:absolute; inset:0;
    background: linear-gradient(90deg,
      rgba(8,42,34,.82) 0%,
      rgba(8,42,34,.55) 42%,
      rgba(8,42,34,.18) 100%);
    pointer-events:none;
  }

  .al-hero__inner{
    position:absolute; inset:0;
    display:flex;
    align-items:flex-end;
  }

  .al-hero__titlebox{
    width: 100%;
    padding: 1.6rem 0 1.35rem;
  }

  .al-hero__titlebox .inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
    color: rgba(255,255,255,.92);
  }

  .al-eyebrow{
    font-size: .86rem;
    letter-spacing: .10em;
    text-transform: uppercase;
    opacity: .88;
    margin: 0 0 .55rem;
  }

  .al-title{
    margin: 0 0 .5rem;
    font-size: 2.35rem;
    line-height: 1.06;
    letter-spacing: .02em;
    max-width: 34ch;
  }

  .al-sub{
    margin: 0;
    max-width: 92ch;
    opacity: .92;
    line-height: 1.65;
    font-size: 1.05rem;
  }

  /* ---------- BODY ---------- */
  .al-body{
    background: var(--cream);
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    padding: 2.2rem 0 3.0rem;
    border-top: 1px solid rgba(0,0,0,.06);
  }

  .al-body .inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
    display: grid;
    gap: 2rem;
  }

  .al-grid-2{
    display:grid;
    grid-template-columns: 1.15fr .85fr;
    gap: 1.6rem;
    align-items: stretch;
  }

  .al-card{
    background: rgba(255,255,255,.55);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
    overflow:hidden;
  }

  .al-card__pad{
    padding: 1.35rem 1.45rem;
  }

  .al-card h2{
    margin: 0 0 .6rem;
    font-size: 1.55rem;
    line-height: 1.2;
    color: var(--ink);
  }

  .al-card p{
    margin: 0 0 .85rem;
    color: rgba(0,0,0,.74);
    line-height: 1.75;
  }

  .al-bullets{
    margin: .25rem 0 0;
    padding-left: 1.15rem;
    color: rgba(0,0,0,.74);
  }
  .al-bullets li{ margin: .35rem 0; }

  /* ---------- Media card (voor code afbeelding) ---------- */
  .al-media{
    display:flex;
    flex-direction: column;
    height: 100%;
  }

  .al-media__img{
    width:100%;
    height: 320px;
    background: rgba(0,0,0,.06);
    overflow:hidden;
  }
  .al-media__img img{
    width:100%;
    height:100%;
    object-fit: cover;
    display:block;
  }

  .al-media__cap{
    padding: 1.0rem 1.2rem;
    border-top: 1px solid rgba(0,0,0,.08);
    color: rgba(0,0,0,.68);
    line-height: 1.6;
  }

  /* ---------- Agenda block (i.p.v. foto) ---------- */
  .agenda{
    padding: 1.15rem 1.2rem;
  }
  .agenda-head{
    display:flex;
    align-items: baseline;
    justify-content: space-between;
    gap: 1rem;
    margin-bottom: .8rem;
  }
  .agenda-head strong{
    font-size: 1.05rem;
    letter-spacing: .06em;
    text-transform: uppercase;
    color: rgba(0,0,0,.70);
  }
  .agenda-note{
    font-size: .95rem;
    color: rgba(0,0,0,.62);
  }

  .agenda-list{
    display:grid;
    gap: .65rem;
    margin: 0;
    padding: 0;
    list-style: none;
  }
  .agenda-item{
    display:grid;
    grid-template-columns: 140px 1fr;
    gap: .9rem;
    padding: .75rem .85rem;
    border-radius: 14px;
    border: 1px solid rgba(0,0,0,.08);
    background: rgba(255,255,255,.65);
  }
  .agenda-date{
    font-weight: 700;
    color: rgba(0,0,0,.78);
  }
  .agenda-where{
    color: rgba(0,0,0,.72);
    line-height: 1.45;
  }
  .agenda-where small{
    display:block;
    color: rgba(0,0,0,.58);
    margin-top: .1rem;
  }

  .agenda-empty{
    padding: .9rem .95rem;
    border-radius: 14px;
    border: 1px dashed rgba(0,0,0,.18);
    background: rgba(255,255,255,.55);
    color: rgba(0,0,0,.62);
  }

  /* ---------- Simple “gallery” voor lezingfoto’s onderaan ---------- */
  .al-gallery{
    display:grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 1rem;
  }
  .al-gallery figure{
    margin:0;
    border-radius: 18px;
    overflow:hidden;
    border: 1px solid rgba(0,0,0,.08);
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
    background: rgba(255,255,255,.55);
  }
  .al-gallery img{
    width:100%;
    height: 240px;
    object-fit: cover;
    display:block;
  }
  .al-gallery figcaption{
    padding: .75rem .85rem;
    color: rgba(0,0,0,.68);
    line-height: 1.55;
    font-size: .95rem;
  }

  @media (max-width: 980px){
    .al-title{ font-size: 2.0rem; }
    .al-grid-2{ grid-template-columns: 1fr; }
    .al-media__img{ height: 280px; }
    .agenda-item{ grid-template-columns: 1fr; }
    .al-gallery{ grid-template-columns: 1fr; }
    .al-gallery img{ height: 300px; }
  }
</style>

<div class="al">

  <!-- HERO -->
  <header class="al-hero">
    <div class="al-hero__media">
      <!-- ✅ upload deze als: /images/artikels-hero.jpg -->
      <img src="{{ '/images/artikels-hero.jpg' | relative_url }}" alt="Artikels en lezingen">
      <div class="al-hero__shade"></div>

      <div class="al-hero__inner">
        <div class="al-hero__titlebox">
          <div class="inner">
            <div class="al-eyebrow">Eco-GenX · Over</div>
            <h1 class="al-title">Artikels, lezingen & publiekswerk</h1>
            <p class="al-sub">
              Praktijkgerichte communicatie: van OVAM-richtlijnen en “code van goede praktijk”
              tot lezingen en Q&A’s voor burgers — helder, correct en met nuance.
            </p>
          </div>
        </div>
      </div>
    </div>
  </header>

  <!-- BODY -->
  <section class="al-body">
    <div class="inner">

      <!-- ROW 1: Artikels/Code -->
      <div class="al-grid-2">

        <div class="al-card">
          <div class="al-card__pad">
            <h2>Code van goede praktijk (OVAM)</h2>
            <p>
              Ik schreef een praktijkgerichte “code van goede praktijk” (OVAM-context) die helpt om
              meetdata, onzekerheden en beslissingslogica correct te interpreteren — en te vertalen naar
              stappen waar stakeholders echt mee verder kunnen.
            </p>
            <ul class="al-bullets">
              <li>heldere definities en afbakening (wat wel/niet kan je besluiten)</li>
              <li>multi-line-of-evidence: meten → begrijpen → bijsturen</li>
              <li>focus op reproduceerbaarheid en verdedigbare keuzes</li>
            </ul>
            <p style="margin-top:.9rem; color: rgba(0,0,0,.62);">
              Upload hier gerust een afbeelding/scan van de cover of een pagina als visuele teaser.
            </p>
          </div>
        </div>

        <div class="al-card al-media">
          <div class="al-media__img">
            <!-- ✅ upload deze als: /images/code-van-goede-praktijk.jpg -->
            <img src="{{ '/images/code-van-goede-praktijk.jpg' | relative_url }}" alt="Code van goede praktijk (OVAM)">
          </div>
          <div class="al-media__cap">
            <strong>Upload-tip:</strong> zet je afbeelding in <code>/images/</code> en noem ze bv.
            <code>code-van-goede-praktijk.jpg</code>. (Mag ook PNG.)
          </div>
        </div>

      </div>

      <!-- ROW 2: Lezingen + agenda (i.p.v. foto) -->
      <div class="al-grid-2">

        <div class="al-card">
          <div class="al-card__pad">
            <h2>Lezingen & sessies voor burgers</h2>
            <p>
              Ik geef lezingen en Q&A’s (bv. PFAS/bodem/water, nature-based oplossingen,
              monitoring en interpretatie). Altijd met ruimte voor vragen en vertaald naar
              “wat betekent dit concreet?”.
            </p>
            <ul class="al-bullets">
              <li>uitleg zonder jargon, met correcte nuance</li>
              <li>praktische handvaten voor vragen en beslissingen</li>
              <li>duiding van meetdata en onzekerheden</li>
            </ul>
          </div>
        </div>

        <div class="al-card">
          <div class="agenda">
            <div class="agenda-head">
              <strong>Agenda</strong>
              <span class="agenda-note">pas aan / voeg regels toe</span>
            </div>

            <!-- ✅ Vervang onderstaande items met je echte data -->
            <ul class="agenda-list">
              <li class="agenda-item">
                <div class="agenda-date">12 feb 2026</div>
                <div class="agenda-where">
                  Lezing Ekeren
                  <small>PFAS & meetdata — interpretatie en vragen</small>
                </div>
              </li>

              <li class="agenda-item">
                <div class="agenda-date">28 mrt 2026</div>
                <div class="agenda-where">
                  Lezing Ronse
                  <small>Bodem & water — nature-based opties</small>
                </div>
              </li>

              <li class="agenda-item">
                <div class="agenda-date">—</div>
                <div class="agenda-where">
                  Boekbaar op aanvraag
                  <small>Gemeenten, burgergroepen, verenigingen</small>
                </div>
              </li>
            </ul>

            <!-- Als je tijdelijk niets wil tonen, vervang de UL hierboven door dit:
            <div class="agenda-empty">Nog geen geplande lezingen. Kom later terug of contacteer me voor een sessie.</div>
            -->

          </div>
        </div>

      </div>

      <!-- ROW 3: optionele fotogalerij (lezingen) -->
      <div class="al-card">
        <div class="al-card__pad">
          <h2>Beelden (optioneel)</h2>
          <p style="color: rgba(0,0,0,.62); margin-bottom: 1rem;">
            Voeg foto’s toe van lezingen/sessies door de bestanden in <code>/images/</code> te zetten en hieronder te linken.
          </p>

          <div class="al-gallery">
            <figure>
              <!-- ✅ upload deze als: /images/lezing-1.jpg -->
              <img src="{{ '/images/lezing-1.jpg' | relative_url }}" alt="Lezingfoto 1">
              <figcaption>Lezing / presentatie — korte caption.</figcaption>
            </figure>

            <figure>
              <!-- ✅ upload deze als: /images/lezing-2.jpg -->
              <img src="{{ '/images/lezing-2.jpg' | relative_url }}" alt="Lezingfoto 2">
              <figcaption>Q&amp;A met burgers — duiding en vragen.</figcaption>
            </figure>

            <figure>
              <!-- ✅ upload deze als: /images/lezing-3.jpg -->
              <img src="{{ '/images/lezing-3.jpg' | relative_url }}" alt="Lezingfoto 3">
              <figcaption>Workshop — praktische handvaten en interpretatie.</figcaption>
            </figure>
          </div>
        </div>
      </div>

    </div>
  </section>

</div>
