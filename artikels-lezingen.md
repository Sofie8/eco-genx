---
title: Artikels & lezingen
layout: default
permalink: /over/artikels-lezingen/
nav:
  order: 6
  tooltip: Artikels & lezingen
---

<style>
  /* =========================================================
     Artikels & lezingen — Eco-GenX style
     Full-width hero (NOT too tall) + content blocks
     Scoped: .al
     ========================================================= */

  /* full width page */
  main{ max-width:none !important; padding:0 !important; overflow:visible !important; }
  main > *, main .content, main article, main .page, main .post{
    max-width:none !important; padding:0 !important; margin:0 !important; overflow:visible !important;
  }

  /* hide default injected page title (theme-dependent) */
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

  /* ---------- HERO (full width, but NOT tall) ---------- */
  .al-hero{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    height: 320px;               /* ✅ minder hoog */
    background: var(--green2);
    overflow: hidden;
    border-bottom: 1px solid rgba(0,0,0,.08);
  }

  .al-hero img{
    width:100%;
    height:100%;
    object-fit: cover;
    object-position: center;
    display:block;
  }

  .al-hero::after{
    content:"";
    position:absolute; inset:0;
    background: linear-gradient(90deg,
      rgba(8,42,34,.86) 0%,
      rgba(8,42,34,.66) 45%,
      rgba(8,42,34,.18) 100%);
    pointer-events:none;
  }

  .al-hero__inner{
    position:absolute;
    inset:0;
    display:flex;
    align-items:flex-end;
    padding: 1.6rem 0 1.2rem;    /* ✅ minder padding */
  }
  .al-hero__inner .inner{
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
    margin-bottom: .55rem;
  }
  .al-title{
    margin: 0 0 .35rem;
    font-size: 2.35rem;
    line-height: 1.08;
    letter-spacing: .02em;
    max-width: 26ch;
  }
  .al-subtitle{
    margin: 0;
    max-width: 78ch;
    opacity: .92;
    line-height: 1.7;
    font-size: 1.02rem;
  }

  /* ---------- BODY WRAP ---------- */
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
  }

  /* ---------- SECTION HEAD ---------- */
  .al-section{
    margin: 0 0 2.0rem;
  }
  .al-section h2{
    margin: 0 0 .6rem;
    font-size: 1.65rem;
    line-height: 1.2;
    color: var(--ink);
  }
  .al-section p{
    margin: 0;
    color: rgba(0,0,0,.74);
    line-height: 1.75;
    max-width: 85ch;
  }

  /* ---------- GRID (cards) ---------- */
  .al-grid{
    display:grid;
    grid-template-columns: 1.1fr .9fr;
    gap: 1.5rem;
    align-items: start;
    margin-top: 1.2rem;
  }

  .al-card{
    background: rgba(255,255,255,.62);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    overflow: hidden;
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
  }

  .al-card__pad{
    padding: 1.25rem 1.35rem;
  }

  .al-card h3{
    margin: 0 0 .45rem;
    font-size: 1.15rem;
    color: var(--ink);
  }

  .al-list{
    margin: .65rem 0 0;
    padding-left: 1.15rem;
    color: rgba(0,0,0,.74);
    line-height: 1.75;
  }
  .al-list li{ margin: .35rem 0; }

  /* image block */
  .al-figure{
    position: relative;
    overflow: hidden;
    background: rgba(0,0,0,.06);
  }
  .al-figure img{
    width: 100%;
    height: 100%;
    display:block;
    object-fit: cover;
  }

  /* for “document/photo” preview cards */
  .al-figure.fixed{
    height: 360px;
  }

  /* ---------- CTA row ---------- */
  .al-cta{
    margin-top: 1.8rem;
    background: rgba(9,45,38,.06);
    border: 1px solid rgba(9,45,38,.12);
    border-radius: 22px;
    padding: 1.35rem 1.35rem;
    display:flex;
    flex-wrap:wrap;
    gap: .9rem 1.1rem;
    align-items:center;
    justify-content: space-between;
  }
  .al-cta strong{
    display:block;
    margin-bottom: .25rem;
    color: var(--ink);
  }
  .al-cta p{
    margin:0;
    color: rgba(0,0,0,.72);
    line-height: 1.7;
    max-width: 75ch;
  }
  .al-btnrow{
    display:flex;
    gap:.75rem;
    flex-wrap:wrap;
  }
  .al-btn{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    padding: .7rem 1rem;
    border-radius: 12px;
    border: 1px solid rgba(11,59,47,.22);
    background: rgba(11,59,47,.06);
    text-decoration:none;
    color: rgba(11,59,47,.92);
    white-space:nowrap;
    font-weight: 600;
  }
  .al-btn:hover{ background: rgba(11,59,47,.10); }

  .al-btn.primary{
    background: rgba(11,59,47,.92);
    border-color: rgba(11,59,47,.92);
    color: rgba(255,255,255,.92);
  }
  .al-btn.primary:hover{ filter: brightness(1.05); }

  /* ---------- RESPONSIVE ---------- */
  @media (max-width: 980px){
    .al-hero{ height: 240px; }
    .al-hero__inner{ padding: 1.2rem 0 1rem; }
    .al-title{ font-size: 1.95rem; }
    .al-grid{ grid-template-columns: 1fr; }
    .al-figure.fixed{ height: 300px; }
  }
</style>

<div class="al">

  <!-- HERO -->
  <section class="al-hero" aria-label="Artikels en lezingen">
    <!-- ✅ upload deze foto als /images/artikels-hero.jpg -->
    <img src="{{ '/images/artikels-hero.jpg' | relative_url }}" alt="Artikels en lezingen">
    <div class="al-hero__inner">
      <div class="inner">
        <div class="al-eyebrow">Over Eco-GenX</div>
        <h1 class="al-title">Artikels & lezingen</h1>
        <p class="al-subtitle">
          Kennisdeling voor burgers, organisaties en overheden — met focus op heldere uitleg, praktische toepasbaarheid
          en meetbaar onderbouwde keuzes.
        </p>
      </div>
    </div>
  </section>

  <!-- BODY -->
  <section class="al-body">
    <div class="inner">

      <!-- INTRO -->
      <div class="al-section">
        <h2>Wat je hier vindt</h2>
        <p>
          Een overzicht van publicaties, presentaties en materiaal dat ik inzet in lezingen en workshops.
          Je kan dit later uitbreiden met PDF’s, links en extra foto’s.
        </p>
      </div>

      <!-- GRID: Code van goede praktijk (OVAM) -->
      <div class="al-section">
        <div class="al-grid">

          <div class="al-card">
            <div class="al-card__pad">
              <h3>Code van goede praktijk (OVAM)</h3>
              <p>
                Ik schreef een code van goede praktijk rond (… jouw onderwerp …). Hier kan je
                een scan/preview tonen en later een downloadlink toevoegen.
              </p>
              <ul class="al-list">
                <li>heldere richtlijnen en toepasbare stappen</li>
                <li>focus op kwaliteit, veiligheid en bewijsvoering</li>
                <li>bruikbaar voor praktijk, beleid en communicatie</li>
              </ul>
            </div>
          </div>

          <div class="al-card">
            <!-- ✅ upload deze foto als /images/code-ovam.jpg (scan/preview) -->
            <div class="al-figure fixed">
              <img src="{{ '/images/code-ovam.jpg' | relative_url }}" alt="Code van goede praktijk (OVAM) preview">
            </div>
            <div class="al-card__pad">
              <p style="margin:0; color: rgba(0,0,0,.68); line-height:1.65;">
                Tip: gebruik een brede screenshot of een nette cover van je document.
              </p>
            </div>
          </div>

        </div>
      </div>

      <!-- GRID: Lezingen -->
      <div class="al-section">
        <div class="al-grid">

          <div class="al-card">
            <div class="al-card__pad">
              <h3>Lezingen & sessies voor burgers</h3>
              <p>
                Ik geef lezingen en Q&A’s (bv. PFAS/bodem/water, nature-based oplossingen, monitoring en interpretatie).
                Altijd met ruimte voor vragen en vertaald naar “wat betekent dit concreet?”.
              </p>
              <ul class="al-list">
                <li>uitleg zonder jargon, met correcte nuance</li>
                <li>praktische handvaten voor vragen en beslissingen</li>
                <li>duiding van meetdata en onzekerheden</li>
              </ul>
            </div>
          </div>

          <div class="al-card">
            <!-- ✅ upload deze foto als /images/lezing-1.jpg -->
            <div class="al-figure fixed">
              <img src="{{ '/images/lezing-1.jpg' | relative_url }}" alt="Lezing / presentatie">
            </div>
            <div class="al-card__pad">
              <p style="margin:0; color: rgba(0,0,0,.68); line-height:1.65;">
                Voeg meerdere lezingfoto’s toe door extra cards te dupliceren (lezing-2.jpg, lezing-3.jpg…).
              </p>
            </div>
          </div>

        </div>
      </div>

      <!-- OPTIONAL: extra row met 3 foto’s -->
      <div class="al-section">
        <h2>Foto’s (optioneel)</h2>
        <p style="margin-bottom:1rem;">
          Wil je een kleine galerij? Upload drie beelden en zet ze hieronder.
        </p>

        <div style="display:grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap:1rem;">
          <div class="al-card">
            <div class="al-figure" style="height:220px;">
              <img src="{{ '/images/lezing-2.jpg' | relative_url }}" alt="Lezing foto 2">
            </div>
          </div>
          <div class="al-card">
            <div class="al-figure" style="height:220px;">
              <img src="{{ '/images/lezing-3.jpg' | relative_url }}" alt="Lezing foto 3">
            </div>
          </div>
          <div class="al-card">
            <div class="al-figure" style="height:220px;">
              <img src="{{ '/images/lezing-4.jpg' | relative_url }}" alt="Lezing foto 4">
            </div>
          </div>
        </div>
      </div>

      <!-- CTA -->
      <div class="al-cta">
        <div>
          <strong>Lezing of sessie organiseren?</strong>
          <p>
            Stuur het thema, doelgroep en context. Dan stel ik een heldere opzet voor met voorbeelden en ruimte voor vragen.
          </p>
        </div>
        <div class="al-btnrow">
          <a class="al-btn primary" href="{{ '/contact/' | relative_url }}">Contacteer mij</a>
          <a class="al-btn" href="{{ '/over/missie-visie/' | relative_url }}">Missie & visie</a>
        </div>
      </div>

    </div>
  </section>

</div>
