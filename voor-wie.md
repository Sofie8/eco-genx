---
title: Voor wie
layout: default
permalink: /over/voor-wie/
---

<style>
  /* =========================================================
     Voor wie — calm split layout (image left, text right)
     NO white card background (text sits on cream background)
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

  /* =========================================================
     HERO — match "Op de agenda" hoogte + tekst wit
     ========================================================= */
  .vw-hero{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    padding: 1.55rem 0 1.15rem;  /* ✅ korter zoals op-de-agenda */
    min-height: 220px;           /* ✅ consistente headerhoogte */
    display: flex;
    align-items: flex-end;

    background: linear-gradient(180deg, rgba(11,59,47,.92), rgba(8,42,34,.92));
    color: #fff;
    border-bottom: 1px solid rgba(0,0,0,.08);
  }

  .vw-hero .inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
  }

  /* forceer wit op alle hero-teksten (ook als globale CSS iets overschrijft) */
  .vw-hero .inner,
  .vw-hero .vw-eyebrow,
  .vw-hero h1,
  .vw-hero p{
    color: rgba(255,255,255,.92) !important;
  }

  .vw-eyebrow{
    font-size: .86rem;
    letter-spacing: .10em;
    text-transform: uppercase;
    opacity: .88;               /* iets helderder */
    margin: 0 0 .55rem;
  }

  .vw-hero h1{
    margin: 0 0 .35rem;
    font-size: 2.25rem;         /* compacter */
    line-height: 1.06;
    letter-spacing: .02em;
  }

  .vw-hero p{
    margin: 0;
    max-width: 80ch;
    opacity: .92;
    line-height: 1.7;
    font-size: 1.02rem;
  }

  /* split */
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
    grid-template-columns: .95fr 1.05fr;
    gap: 1.6rem;
    align-items: start;
  }

  /* left image */
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
    aspect-ratio: 4 / 5;
    background: rgba(0,0,0,.06);
  }
  .vw-photo img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    display:block;
  }

  /* RIGHT: no card, just typography */
  .vw-text{
    padding: .25rem 0 0;
  }

  .vw-text h2{
    margin: 0 0 .7rem;
    font-size: 1.7rem;
    line-height: 1.15;
    color: var(--ink);
  }
  .vw-text p{
    margin: 0 0 1.1rem;
    color: var(--muted);
    line-height: 1.75;
    max-width: 82ch;
  }

  .vw-list{
    margin: .2rem 0 0;
    padding-left: 1.1rem;
    color: rgba(0,0,0,.78);
    line-height: 1.8;
  }
  .vw-list li{ margin: .55rem 0; }
  .vw-list strong{ color: rgba(0,0,0,.86); }

  .vw-cta{
    margin-top: 1.35rem;
    padding-top: 1.1rem;
    border-top: 1px solid rgba(0,0,0,.10);
    display:flex;
    flex-wrap:wrap;
    gap:.8rem;
    align-items:center;
    justify-content: space-between;
  }
  .vw-cta .note{
    color: rgba(0,0,0,.66);
    line-height: 1.6;
    max-width: 72ch;
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
    white-space: nowrap;
  }
  .vw-cta a:hover{ background: rgba(11,59,47,.10); }

  @media (max-width: 980px){
    .vw-hero{
      min-height: 180px;
      padding: 1.2rem 0 1rem;
    }
    .vw-hero h1{ font-size: 1.9rem; }

    .vw-body .inner{ grid-template-columns: 1fr; }
    .vw-photo{ position: static; }
    .vw-photo .frame{ aspect-ratio: 16 / 10; }
  }
</style>

<div class="vw">

  <section class="vw-hero">
    <div class="inner">
      <div class="vw-eyebrow">Over Eco-GenX</div>
      <h1>Voor wie</h1>
    </div>
  </section>

  <section class="vw-body">
    <div class="inner">

      <!-- LEFT -->
      <aside class="vw-photo" aria-label="Sfeerbeeld">
        <div class="frame">
          <img src="{{ '/images/voor-wie.jpg' | relative_url }}" alt="Eco-GenX — veldwerk en interpretatie">
        </div>
      </aside>

      <!-- RIGHT -->
      <article class="vw-text">
        <h2>Decision-ready advies voor…</h2>
        <p>
          Ingenieursbureaus, overheden, terreinbeheerders, bedrijven en burgerinitiatieven
          die een bodem-/watervraagstuk willen oplossen met een aanpak die technisch klopt
          én praktisch werkt.
        </p>

        <ul class="vw-list">
          <li><strong>Overheden & publieke partners</strong> — strategie en prioritering, monitoring & interpretatie, duiding voor communicatie</li>
          <li><strong>Ingenieursbureaus & aannemers</strong> — evidence-plan/KPI’s, proefopzet & evaluatie, veld → rapport → keuze</li>
          <li><strong>Bedrijven & sites</strong> — haalbaarheidsinschatting, risk-based keuzes, verificatie van maatregelen</li>
          <li><strong>Burgers & verenigingen</strong> — lezingen/Q&A, interpretatie van meetdata, praktische handvaten</li>
        </ul>

        <div class="vw-cta">
          <div class="note">
            Twijfel je of jouw case past? Stuur 5 regels + locatie + wat je al gemeten hebt.
          </div>
          <a href="{{ '/contact/' | relative_url }}">Contacteer mij →</a>
        </div>
      </article>

    </div>
  </section>

</div>

