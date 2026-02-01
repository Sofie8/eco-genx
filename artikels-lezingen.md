---
title: Artikels & lezingen
layout: default
permalink: /over/artikels-lezingen/
---

<style>
  /* =========================================================
     ARTIKELS & LEZINGEN — Eco-GenX (full-bleed + cards)
     + FIX: header/nav niet sticky op deze pagina
     ========================================================= */

  /* ---------- FIX: header/navbar mag NIET sticky op deze pagina ---------- */
  header,
  header.background,
  header nav,
  nav.main-nav,
  .site-header,
  .navbar,
  .nav-wrapper{
    position: static !important;
    top: auto !important;
  }
  header.is-sticky,
  header.sticky,
  .sticky,
  .is-sticky{
    position: static !important;
    top: auto !important;
  }
  body{ padding-top: 0 !important; }

  /* ---------- Full width page ---------- */
  main{ max-width:none !important; padding:0 !important; overflow:visible !important; }
  main > *, main .content, main article, main .page, main .post{
    max-width:none !important; padding:0 !important; margin:0 !important; overflow:visible !important;
  }

  .al{
    --max: 1200px;
    --pad: 1.25rem;

    --eco-dark: var(--eco-dark, #0b3b2f);
    --eco-dark-2: var(--eco-dark-2, #082a22);
    --eco-cream: var(--eco-cream, #f6f4ee);

    --ink: rgba(0,0,0,.86);
    --muted: rgba(0,0,0,.66);
    --line: rgba(0,0,0,.10);

    --shadow: 0 14px 36px rgba(0,0,0,.08);
    --shadow2: 0 18px 44px rgba(0,0,0,.10);
  }

  /* ---------- HERO ---------- */
.al-hero{
  position: relative;
  left: 50%; right: 50%;
  width: 100vw;
  margin-left: -50vw; margin-right: -50vw;

  min-height: 520px;
  background: var(--eco-dark-2);
  overflow: hidden;
}

/* full-bleed image stays full width */
.al-hero img{
  width:100%;
  height:100%;
  object-fit: cover;
  display:block;
  min-height: 520px;
}

.al-hero::after{
  content:"";
  position:absolute; inset:0;
  background: linear-gradient(90deg,
    rgba(8,42,34,.86) 0%,
    rgba(8,42,34,.66) 45%,
    rgba(8,42,34,.18) 100%);
}

/* ✅ inner content is LIMITED in width (zoals Projects) */
.al-hero__inner{
  position:absolute;
  inset:0;
  display:flex;
  align-items:flex-end;
  padding: 3.0rem 0 2.4rem;
}

/* ✅ THIS is the key: max width like projects */
.al-hero__content{
  max-width: 1200px;      /* <-- zelfde max als projects */
  width: 100%;
  margin: 0 auto;
  padding: 0 1.25rem;     /* <-- zelfde padding als projects */
  color: rgba(255,255,255,.92);
}

/* make title block not too wide */
.al-title{
  margin: 0 0 .6rem;
  font-size: 3rem;
  line-height: 1.04;
  letter-spacing: .02em;
  max-width: 20ch;        /* ✅ iets compacter */
}

.al-lead{
  margin: 0;
  max-width: 70ch;        /* ✅ compacter zoals projects */
  line-height: 1.7;
  opacity: .92;
  font-size: 1.06rem;
}

/* responsive */
@media (max-width: 980px){
  .al-title{ font-size: 2.25rem; max-width: 22ch; }
  .al-lead{ max-width: 68ch; }
}

  /* ---------- BODY ---------- */
  .al-body{
    background: var(--eco-cream);
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;
    padding: 2.6rem 0 3.4rem;
    border-top: 1px solid rgba(0,0,0,.06);
  }
  .al-body__inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
    display: grid;
    grid-template-columns: 1.1fr .9fr;
    gap: 1.8rem;
    align-items: start;
  }

  .panel{
    background: rgba(255,255,255,.62);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    box-shadow: var(--shadow);
    overflow: hidden;
  }
  .panel__head{
    padding: 1.25rem 1.35rem 1.05rem;
    border-bottom: 1px solid rgba(0,0,0,.06);
  }
  .panel__head h2{
    margin: 0 0 .35rem;
    font-size: 1.45rem;
    color: var(--ink);
  }
  .panel__head p{
    margin: 0;
    color: var(--muted);
    line-height: 1.7;
    max-width: 75ch;
  }

  .panel__body{
    padding: 1.25rem 1.35rem 1.35rem;
  }

  /* media block inside panel */
  .media{
    border-radius: 16px;
    overflow: hidden;
    border: 1px solid rgba(0,0,0,.08);
    background: rgba(0,0,0,.04);
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
  }
  .media img{
    width:100%;
    height: 320px;
    object-fit: cover;
    display:block;
  }
  .media .cap{
    padding: .85rem .95rem;
    color: var(--muted);
    line-height: 1.65;
    background: rgba(255,255,255,.70);
  }

  /* cards list */
  .cards{
    display: grid;
    grid-template-columns: 1fr;
    gap: 1rem;
  }
  .card{
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 16px;
    padding: 1rem 1.05rem;
    background: rgba(255,255,255,.55);
    box-shadow: 0 14px 36px rgba(0,0,0,.05);
  }
  .card h3{
    margin: 0 0 .35rem;
    font-size: 1.1rem;
    color: var(--ink);
  }
  .card p{
    margin: 0;
    color: var(--muted);
    line-height: 1.65;
  }

  .list{
    margin: .75rem 0 0;
    padding-left: 1.2rem;
    color: rgba(0,0,0,.74);
  }
  .list li{ margin: .35rem 0; }

  /* CTA */
  .al-cta{
    margin-top: 1.4rem;
    padding: 1.25rem 1.35rem;
    border-radius: 18px;
    border: 1px solid rgba(11,59,47,.18);
    background: rgba(11,59,47,.08);
  }
  .al-cta h3{ margin: 0 0 .35rem; color: var(--ink); }
  .al-cta p{ margin: 0; color: var(--muted); line-height: 1.7; }
  .btnrow{
    display:flex;
    gap:.7rem;
    flex-wrap:wrap;
    margin-top: .95rem;
  }
  .btn{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    padding: .65rem .95rem;
    border-radius: 12px;
    text-decoration:none;
    border: 1px solid rgba(11,59,47,.22);
    background: rgba(11,59,47,.10);
    color: rgba(11,59,47,.92);
    font-weight: 600;
  }
  .btn:hover{ background: rgba(11,59,47,.14); }

  @media (max-width: 980px){
    .al-title{ font-size: 2.25rem; }
    .al-body__inner{ grid-template-columns: 1fr; }
    .media img{ height: 280px; }
  }
</style>

<div class="al">

  <!-- HERO -->
  <section class="al-hero">
    <img src="{{ '/images/artikels-hero.jpg' | relative_url }}" alt="Lezingen en kennisdeling Eco-GenX">
    <div class="al-hero__inner">
      <div class="al-hero__content">
        <div class="al-eyebrow">Over Eco-GenX · Artikels & lezingen</div>
        <h1 class="al-title">Kennis, praktijk & communicatie</h1>
        <p class="al-lead">
          Ik deel inzichten uit fytotechnologie, bodem- en milieumicrobiologie en data-gedreven monitoring —
          via richtlijnen, artikels en lezingen voor professionals én burgers.
        </p>
      </div>
    </div>
  </section>

  <!-- BODY -->
  <section class="al-body">
    <div class="al-body__inner">

      <!-- LEFT: Code van Goede Praktijk -->
      <div class="panel">
        <div class="panel__head">
          <h2>Code van Goede Praktijk Fytoremediatie (OVAM)</h2>
          <p>
            Ik was mede-auteur van een praktijkgerichte handleiding om fytoremediatie correct en efficiënt toe te passen in Vlaanderen.
            Van ontwerpkeuzes tot monitoring en kwaliteitsbewaking.
          </p>
        </div>

        <div class="panel__body">
          <div class="media">
            <img src="{{ '/images/code-ovam-cover.jpg' | relative_url }}" alt="Cover Code van Goede Praktijk Fytoremediatie">
            <div class="cap">
              Upload hier je cover/scan. Bestandsnaam-tip: <strong>images/code-ovam-cover.jpg</strong>
              (of pas het pad hierboven aan).
            </div>
          </div>

          <ul class="list">
            <li>praktische richtlijnen voor ontwerp en implementatie</li>
            <li>risico’s beheersen met meetbaar bewijs</li>
            <li>monitoring: wat, wanneer en waarom meten</li>
          </ul>

          <div class="al-cta">
            <h3>Wil je dit toepassen op jouw site?</h3>
            <p>Stuur je context en doel. Dan vertaal ik richtlijnen naar een evidence-plan met haalbare stappen.</p>
            <div class="btnrow">
              <a class="btn" href="{{ '/contact/' | relative_url }}">Contacteer mij →</a>
              <a class="btn" href="{{ '/restore/' | relative_url }}">Bekijk Restore →</a>
            </div>
          </div>
        </div>
      </div>

      <!-- RIGHT: Artikels + lezingen (cards) -->
      <div class="panel">
        <div class="panel__head">
          <h2>Lezingen & communicatie</h2>
          <p>
            Voor burgers, bedrijven en organisaties: helder, onderbouwd en toepasbaar.
            Voeg hieronder makkelijk foto’s/links toe per lezing of artikel.
          </p>
        </div>

        <div class="panel__body">
          <div class="cards">

            <div class="card">
              <h3>Lezing · Bodem als levend systeem</h3>
              <p>Korte intro (plaats, doelgroep, thema). Voeg een foto toe of link later.</p>
            </div>

            <div class="card">
              <h3>Lezing · PFAS & nature-based herstel</h3>
              <p>Hoe combineer je risico, meetplan en realistische interventies — met transparante monitoring.</p>
            </div>

            <div class="card">
              <h3>Artikel / bijdrage · Praktijk & beleid</h3>
              <p>Snippets van publicaties of bijdragen (met eventueel download/link later).</p>
            </div>

          </div>

          <div style="margin-top:1rem;" class="media">
            <img src="{{ '/images/lezing-01.jpg' | relative_url }}" alt="Foto van een lezing of workshop">
            <div class="cap">
              Upload een lezingfoto als <strong>images/lezing-02.jpg</strong> (of pas het pad aan).
              Wil je meerdere? Ik kan er een mooie gallery van maken.
            </div>
          </div>

        </div>
      </div>

    </div>
  </section>

</div>
