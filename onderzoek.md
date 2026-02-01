---
title: Onderzoek & ontwikkeling
layout: default
permalink: /onderzoek/
# 1 groepsafbeelding met logo's (wordt in ELKE accordion-content getoond)
logo_group: /images/onderzoek-logos.png
---

<style>
  /* =========================================================
     ONDERZOEK — Eco-GenX style (Isodetect-ish)
     - hero even hoog als Artikels banner
     - alles links uitgelijnd
     - accordions met + / –
     - logo-groep per item (1 image)
     ========================================================= */

  /* full width page */
  main{ max-width:none !important; padding:0 !important; overflow:visible !important; text-align:left !important; }
  main > *, main .content, main article, main .page, main .post{
    max-width:none !important; padding:0 !important; margin:0 !important; overflow:visible !important;
    text-align:left !important;
  }

  /* hide default injected page title (theme-dependent) */
  .page-title,
  .page-header,
  .page-header h1,
  h1.page-title,
  main > h1:first-child{
    display:none !important;
  }

  /* ✅ HEADER/NAV mag NIET fixed/sticky op deze pagina */
  header,
  header.background,
  .site-header,
  .header{
    position: relative !important;
    top: auto !important;
  }
  body{ padding-top: 0 !important; }

  .rd{
    --max: 1200px;
    --pad: 1.25rem;
    --cream: var(--eco-cream, #f6f4ee);
    --green: var(--eco-dark, #0b3b2f);
    --green2: var(--eco-dark-2, #082a22);
    --ink: rgba(0,0,0,.86);
    --muted: rgba(0,0,0,.66);
    --line: rgba(0,0,0,.10);
    --card: rgba(255,255,255,.62);
    --shadow: 0 14px 36px rgba(0,0,0,.06);
  }

  /* ---------- HERO (zelfde hoogte vibe als Artikels) ---------- */
  .rd-hero{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    height: 320px;
    background: var(--green2);
    overflow: hidden;
    border-bottom: 1px solid rgba(0,0,0,.08);
  }
  .rd-hero img{
    width:100%;
    height:100%;
    object-fit: cover;
    object-position: center;
    display:block;
  }
  .rd-hero::after{
    content:"";
    position:absolute; inset:0;
    background: linear-gradient(90deg,
      rgba(8,42,34,.86) 0%,
      rgba(8,42,34,.66) 45%,
      rgba(8,42,34,.18) 100%);
    pointer-events:none;
  }
  .rd-hero__inner{
    position:absolute;
    inset:0;
    display:flex;
    align-items:flex-end;
    padding: 1.6rem 0 1.2rem;
  }
  .rd-hero__inner .inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
    color: rgba(255,255,255,.92);
    text-align:left !important;
  }
  .rd-eyebrow{
    font-size: .86rem;
    letter-spacing: .10em;
    text-transform: uppercase;
    opacity: .88;
    margin-bottom: .55rem;
  }
  .rd-title{
    margin: 0 0 .35rem;
    font-size: 2.35rem;
    line-height: 1.08;
    letter-spacing: .02em;
    max-width: 28ch;
  }
  .rd-subtitle{
    margin: 0;
    max-width: 90ch;
    opacity: .92;
    line-height: 1.7;
    font-size: 1.02rem;
  }

  /* ---------- BODY WRAP ---------- */
  .rd-body{
    background: var(--cream);
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;
    padding: 2.2rem 0 3.0rem;
    border-top: 1px solid rgba(0,0,0,.06);
  }
  .rd-body .inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
    text-align:left !important;
  }

  /* ---------- SECTION HEAD ---------- */
  .rd-section{ margin: 0 0 2.2rem; }
  .rd-section h2{
    margin: 0 0 .6rem;
    font-size: 1.65rem;
    line-height: 1.2;
    color: var(--ink);
    text-align:left !important;
  }
  .rd-section p{
    margin: 0 0 1rem;
    color: rgba(0,0,0,.74);
    line-height: 1.75;
    max-width: 92ch;
    text-align:left !important;
  }
  .rd-divider{
    height: 1px;
    background: rgba(0,0,0,.10);
    margin: 1.0rem 0 1.2rem;
  }

  /* ---------- ACCORDION LIST ---------- */
  .rd-list{ display:flex; flex-direction:column; gap: 1rem; }

  details.rd-item{
    background: var(--card);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    box-shadow: var(--shadow);
    overflow: hidden;
  }

  summary.rd-sum{
    list-style: none;
    cursor: pointer;
    display: grid;
    grid-template-columns: 46px 1fr 52px;
    gap: .85rem;
    align-items: center;
    padding: 1.05rem 1.15rem;
    background: rgba(0,0,0,.04);
  }
  summary.rd-sum::-webkit-details-marker{ display:none; }

  /* left icon (chevron) */
  .rd-chev{
    width: 30px; height: 30px;
    border-radius: 999px;
    border: 1px solid rgba(0,0,0,.14);
    display:flex;
    align-items:center;
    justify-content:center;
    background: rgba(255,255,255,.55);
    font-size: 18px;
    line-height: 1;
    transform: translateY(1px);
  }
  details[open] .rd-chev{ transform: translateY(1px) rotate(90deg); }

  /* title + sub */
  .rd-sum strong{
    display:block;
    font-size: 1.08rem;
    line-height: 1.3;
    color: rgba(0,0,0,.86);
    text-align:left !important;
  }
  .rd-sum span{
    display:block;
    margin-top: .25rem;
    color: rgba(0,0,0,.62);
    line-height: 1.6;
    text-align:left !important;
  }

  /* plus/minus button */
  .rd-plus{
    width: 38px; height: 38px;
    border-radius: 999px;
    border: 1px solid rgba(0,0,0,.16);
    background: rgba(255,255,255,.55);
    position: relative;
    justify-self: end;
  }
  .rd-plus::before,
  .rd-plus::after{
    content:"";
    position:absolute;
    left: 50%; top: 50%;
    width: 16px; height: 2px;
    background: rgba(0,0,0,.55);
    transform: translate(-50%, -50%);
  }
  .rd-plus::after{
    transform: translate(-50%, -50%) rotate(90deg);
  }
  details[open] .rd-plus::after{ display:none; } /* open => minus */

  /* content area */
  .rd-content{
    padding: 1.15rem 1.25rem 1.25rem;
    background: rgba(255,255,255,.35);
    border-top: 1px solid rgba(0,0,0,.08);
    text-align:left !important;
  }
  .rd-content p{
    margin: 0 0 .85rem;
    color: rgba(0,0,0,.74);
    line-height: 1.75;
    text-align:left !important;
  }
  .rd-content ul{
    margin: .2rem 0 0;
    padding-left: 1.1rem;
    color: rgba(0,0,0,.74);
    line-height: 1.75;
    text-align:left !important;
  }

  /* ✅ logo group (1 image) shown inside each open item */
  .rd-logos{
    margin: 0 0 1rem;
    padding: .7rem .8rem;
    border-radius: 14px;
    border: 1px solid rgba(0,0,0,.10);
    background: rgba(255,255,255,.45);
    display:flex;
    align-items:center;
    justify-content:flex-start;
    gap: .75rem;
  }
  .rd-logos img{
    width: 100%;
    max-width: 620px;     /* looks like a “logo strip” */
    height: auto;
    display:block;
    object-fit: contain;
  }
  /* if you want it bigger, raise max-width */

  /* archive block title */
  .rd-arch-note{
    font-size: .98rem;
    color: rgba(0,0,0,.68);
    margin-top: .25rem;
  }

  @media (max-width: 980px){
    .rd-hero{ height: 240px; }
    .rd-title{ font-size: 1.95rem; }
    summary.rd-sum{ grid-template-columns: 42px 1fr 48px; }
    .rd-logos img{ max-width: 100%; }
  }
</style>

<div class="rd">

  <!-- HERO -->
  <section class="rd-hero" aria-label="Onderzoek & ontwikkeling">
    <img src="{{ '/images/onderzoek-hero.jpg' | relative_url }}" alt="Onderzoek & ontwikkeling">
    <div class="rd-hero__inner">
      <div class="inner">
        <div class="rd-eyebrow">Eco-GenX · onderzoek & ontwikkeling</div>
        <h1 class="rd-title">Van wetenschap naar terrein</h1>
        <p class="rd-subtitle">
          Ik ontwikkel en test meetbare innovaties rond bodem-, water- en PFAS-herstel:
          nature-based ontwerpen, evidence-plannen en monitoring die decision-ready antwoorden opleveren.
        </p>
      </div>
    </div>
  </section>

  <!-- BODY -->
  <section class="rd-body">
    <div class="inner">

      <!-- LOPENDE PROJECTEN — ECO-GENX -->
      <div class="rd-section" id="lopend-ecogenx">
        <h2>Lopende projecten — Eco-GenX</h2>
        <p>
          Projecten waarbij ik betrokken ben via Eco-GenX / vennootschap (advies, ontwerp, monitoring, proof-of-impact).
        </p>
        <div class="rd-divider"></div>

        <div class="rd-list">

          <!-- Barebeek -->
          <details class="rd-item" open>
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <strong>Barebeek (Zemst) — PFAS piloot & demonstratie</strong>
                <span>Nature-based ingrepen om PFAS-vang efficiënter te maken in de sedimentvang, met multi-line-of-evidence monitoring.</span>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>

            <div class="rd-content">
              {% if page.logo_group %}
                <div class="rd-logos">
                  <img src="{{ page.logo_group | relative_url }}" alt="Partners / organisaties">
                </div>
              {% endif %}

              <p>
                Piloot- en demonstratietraject om de PFAS-vangefficiëntie in de sedimentvang significant te verhogen met een hybride
                fytoremediatieconcept: drijvende zuiveringseilanden (FTW’s), gerichte oeverbeplanting en (waar relevant) reactief substraat. :contentReference[oaicite:2]{index=2}
              </p>
              <p>
                Effectiviteit wordt onderbouwd via een monitoringsprogramma met concentratie- én fluxmetingen (o.a. iFLUX),
                hydraulische opvolging en ecologische observaties — zodat saneringseffect en grondwaterveiligheid objectief aantoonbaar zijn. :contentReference[oaicite:3]{index=3}
              </p>

              <ul>
                <li>Fasering: nulmeting → ontwerp → real-scale implementatie → effectmonitoring</li>
                <li>Output: decision-ready evaluatie + richtlijnen voor opschaling</li>
              </ul>
            </div>
          </details>

          <!-- PFAS Resolve (voorbeeld) -->
          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <strong>PFAS RESOLVE — evidence & monitoring (voorbeeld)</strong>
                <span>Korte uitleg wat jij wil tonen (later aanvullen).</span>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>

            <div class="rd-content">
              {% if page.logo_group %}
                <div class="rd-logos">
                  <img src="{{ page.logo_group | relative_url }}" alt="Partners / organisaties">
                </div>
              {% endif %}

              <p>
                Vul hier later details aan: doel, aanpak, deliverables, partners, status.
              </p>
              <ul>
                <li>Deliverable 1</li>
                <li>Deliverable 2</li>
              </ul>
            </div>
          </details>

        </div>
      </div>

      <!-- LOPENDE ACADEMISCHE PROJECTEN — UHASSELT -->
      <div class="rd-section" id="lopend-academisch">
        <h2>Lopende academische projecten — UHasselt (20%)</h2>
        <p>
          Projecten waarbij ik betrokken ben via UHasselt (wetenschappelijke onderbouwing, methodologie, interpretatie).
        </p>
        <div class="rd-divider"></div>

        <div class="rd-list">
          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <strong>Academisch project (template)</strong>
                <span>1 zin: doel + waarom relevant.</span>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>

            <div class="rd-content">
              {% if page.logo_group %}
                <div class="rd-logos">
                  <img src="{{ page.logo_group | relative_url }}" alt="Partners / organisaties">
                </div>
              {% endif %}

              <p>Voeg hier je korte beschrijving toe.</p>
              <ul>
                <li>Rol: …</li>
                <li>Focus: …</li>
                <li>Status: …</li>
              </ul>
            </div>
          </details>
        </div>
      </div>

      <!-- ARCHIEF -->
      <div class="rd-section" id="archief">
        <h2>Archief (2019–2024)</h2>
        <p class="rd-arch-note">
          Afgeronde of oudere projecten. (Als je later wél wil splitsen bedrijf/academisch: maak gewoon 2 kolommen of 2 lijsten binnen dit archief.)
        </p>
        <div class="rd-divider"></div>

        <div class="rd-list">
          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <strong>2019–2024 — selecties</strong>
                <span>Klik open voor voorbeelden (dupliceer items en vul aan).</span>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>

            <div class="rd-content">
              {% if page.logo_group %}
                <div class="rd-logos">
                  <img src="{{ page.logo_group | relative_url }}" alt="Partners / organisaties">
                </div>
              {% endif %}

              <ul>
                <li><strong>Projecttitel</strong> — 1 zin: wat was het + jouw rol.</li>
                <li><strong>Projecttitel</strong> — 1 zin: wat was het + jouw rol.</li>
                <li><strong>Projecttitel</strong> — 1 zin: wat was het + jouw rol.</li>
              </ul>
            </div>
          </details>
        </div>
      </div>

    </div>
  </section>
</div>
