---
title: Onderzoek & ontwikkeling
layout: default
permalink: /over/onderzoek/
nav:
  order: 5
  tooltip: Onderzoek
---

<style>
  /* =========================================================
     Onderzoek & Ontwikkeling — Eco-GenX style
     Scoped: .rd (dus geen globale chaos)
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

  .rd{
    --max: 1200px;
    --pad: 1.25rem;
    --cream: var(--eco-cream, #f6f4ee);
    --green: var(--eco-dark, #0b3b2f);
    --green2: var(--eco-dark-2, #082a22);
    --ink: rgba(0,0,0,.86);
    --muted: rgba(0,0,0,.66);
    --line: rgba(0,0,0,.10);
  }

  /* hard: keep text left in this page */
  .rd, .rd *{ text-align:left !important; }

  /* ---------- HERO (like artikels, not too tall) ---------- */
  .rd-hero{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    height: 320px;
    background: var(--green2);
    overflow:hidden;
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
    max-width: 80ch;
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
    padding: 2.2rem 0 3.2rem;
    border-top: 1px solid rgba(0,0,0,.06);
  }
  .rd-body .inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
  }

  /* ---------- Intro block (like Isodetect) ---------- */
  .rd-intro{
    display:grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    padding: 1.25rem 0 1.25rem;
  }
  .rd-intro h2{
    margin: 0 0 .75rem;
    font-size: 2rem;
    line-height: 1.1;
    letter-spacing: .01em;
    color: var(--ink);
  }
  .rd-intro p{
    margin: 0;
    color: rgba(0,0,0,.74);
    line-height: 1.8;
    font-size: 1.05rem;
    max-width: 70ch;
  }

  /* Divider */
  .rd-divider{
    height: 1px;
    background: rgba(0,0,0,.10);
    margin: 1.25rem 0 1.35rem;
  }

  /* ---------- Section head ---------- */
  .rd-section{
    margin-top: 1.6rem;
  }
  .rd-section h2{
    margin: 0 0 .55rem;
    font-size: 1.75rem;
    line-height: 1.2;
    color: var(--ink);
  }
  .rd-section p.lead{
    margin: 0 0 1.2rem;
    color: rgba(0,0,0,.74);
    line-height: 1.75;
    max-width: 92ch;
  }

  /* ---------- Accordion list ---------- */
  .rd-acc{
    display:flex;
    flex-direction:column;
    gap: .9rem;
  }

  details.rd-item{
    background: rgba(255,255,255,.62);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
    overflow: hidden;
  }

  summary.rd-sum{
    list-style: none;
    cursor: pointer;
    display:grid;
    grid-template-columns: 40px 1fr 42px;
    gap: 1rem;
    align-items: start;
    padding: 1.05rem 1.15rem;
    background: rgba(0,0,0,.04);
  }

  /* remove default marker */
  summary.rd-sum::-webkit-details-marker{ display:none; }

  .rd-chev{
    width: 28px; height: 28px;
    border-radius: 999px;
    display:flex;
    align-items:center;
    justify-content:center;
    color: rgba(0,0,0,.72);
    border: 1px solid rgba(0,0,0,.18);
    background: rgba(255,255,255,.7);
    margin-top: .1rem;
  }

  .rd-sum h3{
    margin: 0 0 .15rem;
    font-size: 1.1rem;
    line-height: 1.3;
    color: var(--ink);
  }
  .rd-sum p{
    margin: 0;
    color: rgba(0,0,0,.70);
    line-height: 1.6;
  }

  .rd-plus{
    width: 36px; height: 36px;
    border-radius: 999px;
    display:flex;
    align-items:center;
    justify-content:center;
    border: 1px solid rgba(0,0,0,.18);
    background: rgba(255,255,255,.72);
    color: rgba(0,0,0,.72);
    font-size: 1.15rem;
  }

  details[open] .rd-plus{ font-size: 1.35rem; }
  details[open] .rd-plus::before{ content:"–"; }
  details:not([open]) .rd-plus::before{ content:"+"; }

  details[open] .rd-chev{
    transform: rotate(90deg);
    transition: transform .15s ease;
  }

  .rd-bodybox{
    padding: 1.05rem 1.15rem 1.15rem;
    background: rgba(255,255,255,.55);
  }

  .rd-grid{
    display:grid;
    grid-template-columns: 1fr;
    gap: .9rem;
  }

  .rd-meta{
    display:grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: .65rem 1rem;
    padding-top: .2rem;
  }
  .rd-kv{
    border-top: 1px solid rgba(0,0,0,.08);
    padding-top: .55rem;
  }
  .rd-k{
    font-size: .82rem;
    letter-spacing: .08em;
    text-transform: uppercase;
    opacity: .7;
    margin-bottom: .15rem;
  }
  .rd-v{
    color: rgba(0,0,0,.76);
    line-height: 1.6;
  }

  /* Logos per project (one grouped image) */
  .rd-logos{
    margin-top: .95rem;
    border-top: 1px solid rgba(0,0,0,.08);
    padding-top: .85rem;
  }
  .rd-logos .label{
    font-size: .82rem;
    letter-spacing: .08em;
    text-transform: uppercase;
    opacity: .7;
    margin: 0 0 .55rem;
  }
  .rd-logos img{
    width: 100%;
    max-width: 820px;
    height: auto;
    border-radius: 14px;
    border: 1px solid rgba(0,0,0,.08);
    background: rgba(255,255,255,.7);
  }

  /* Archive badge row (optional) */
  .rd-note{
    margin-top: .65rem;
    color: rgba(0,0,0,.70);
    line-height: 1.7;
    max-width: 95ch;
  }

  @media (max-width: 980px){
    .rd-hero{ height: 240px; }
    .rd-title{ font-size: 1.95rem; }
    .rd-intro{ grid-template-columns: 1fr; gap: 1.2rem; }
    .rd-meta{ grid-template-columns: 1fr; }
    summary.rd-sum{ grid-template-columns: 34px 1fr 42px; }
  }
</style>

<div class="rd">

  <!-- HERO -->
  <section class="rd-hero" aria-label="Onderzoek en ontwikkeling">
    <img src="{{ '/images/onderzoek-hero.jpg' | relative_url }}" alt="Onderzoek & ontwikkeling">
    <div class="rd-hero__inner">
      <div class="inner">
        <div class="rd-eyebrow">Eco-GenX · Onderzoek & ontwikkeling</div>
        <h1 class="rd-title">Van wetenschap naar terrein</h1>
        <p class="rd-subtitle">
          Ik vertaal fundamentele inzichten naar decision-ready toepassingen voor bodem, water en PFAS-herstel —
          met focus op meetbaarheid, monitoring en reproduceerbare aanpak.
        </p>
      </div>
    </div>
  </section>

  <!-- BODY -->
  <section class="rd-body">
    <div class="inner">

      <!-- Intro block (zoals Isodetect, maar op maat) -->
      <div class="rd-intro">
        <div>
          <h2>Onderzoek als motor voor praktijk</h2>
          <p>
            Via Eco-GenX ontwikkel en test ik nature-based oplossingen in real-life context:
            fytoremediatie, plant-microbe interacties, (e)DNA-gebaseerde proof-of-impact en
            multi-line-of-evidence monitoring voor bodem- en watersystemen.
          </p>
        </div>
        <div>
          <h2>Ook academisch sterk verankerd</h2>
          <p>
            Als postdoc met een 20% aanstelling bij UHasselt blijf ik nauw betrokken bij fundamentele
            onderzoeksprojecten en methodologische vernieuwing. Die kennis stroomt rechtstreeks door
            naar Eco-GenX: sneller leren, beter ontwerp, scherpere interpretatie en robuustere besluitvorming.
          </p>
        </div>
      </div>

      <div class="rd-divider"></div>

      <!-- SECTION 1 -->
      <div class="rd-section">
        <h2>Huidige onderzoek & ontwikkelingsprojecten (via Eco-GenX)</h2>
        <p class="lead">
          Projecten waarbij ik betrokken ben via Eco-GenX / vennootschap: advies, ontwerp, monitoring en proof-of-impact.
        </p>

        <div class="rd-acc">

          <!-- Barebeek -->
          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>Barebeek (Zemst) — PFAS piloot & demonstratie (2025–2028)</h3>
                <p>Nature-based ingrepen om PFAS-vang in sedimentvang te verhogen, met multi-line-of-evidence monitoring.</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>

            <div class="rd-bodybox">
              <div class="rd-meta">
                <div class="rd-kv">
                  <div class="rd-k">Locatie & scope</div>
                  <div class="rd-v">Barebeek (Zemst) — in-situ piloot/demonstratie (VMM).</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Verontreiniging</div>
                  <div class="rd-v">PFAS</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Rol & expertise</div>
                  <div class="rd-v">
                    Expert plant–microbe interacties voor PFAS sorptie/extractie.
                    Haalbaarheidsstudie, experimenteel design en data-interpretatie (constructed floating wetlands).
                  </div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Highlights</div>
                  <div class="rd-v">
                    In-situ aanpak om PFAS-vang efficiëntie significant te verhogen met o.a. floating treatment wetlands,
                    oeverbeplanting en (waar passend) reactief substraat, gekoppeld aan monitoring van concentraties én fluxen
                    richting grondwater/oppervlaktewater (o.a. iFLUX).
                  </div>
                </div>
              </div>

              <!-- per project 1 grouped logo image -->
              <!-- Upload bv: /images/onderzoek/logos-barebeek.jpg -->
              <div class="rd-logos">
                <p class="label">Partners (logo’s)</p>
                <img src="{{ '/images/onderzoek/logos-barebeek.jpg' | relative_url }}" alt="Partners Barebeek">
              </div>
            </div>
          </details>

          <!-- PFAS RESOLVE -->
          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>Interreg PFAS RESOLVE (2024–2027)</h3>
                <p>Veldpilots: plant-gebaseerde staalname + draagbare biosensor voor snelle, kostenefficiënte kartering.</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>

            <div class="rd-bodybox">
              <div class="rd-meta">
                <div class="rd-kv">
                  <div class="rd-k">Locatie & scope</div>
                  <div class="rd-v">Grensoverschrijdende regio Maas-Rijn</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Verontreiniging</div>
                  <div class="rd-v">PFAS (incl. PFOS, PFOA, GenX)</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Rol & expertise</div>
                  <div class="rd-v">Verantwoordelijk voor phyto-screening en veldpilots (in opdracht van bio2clean).</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Highlights</div>
                  <div class="rd-v">
                    Opzet van veldpilots waarin plant-gebaseerde staalname wordt gecombineerd met een nieuwe, draagbare biosensor.
                    Snel alternatief voor klassieke labanalyses bij grootschalige kartering.
                  </div>
                </div>
              </div>

              <div class="rd-logos">
                <p class="label">Partners (logo’s)</p>
                <img src="{{ '/images/onderzoek/logos-pfas-resolve.jpg' | relative_url }}" alt="Partners PFAS RESOLVE">
              </div>
            </div>
          </details>

          <!-- LIFE NARMENA -->
          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>LIFE NARMENA (2020–2026)</h3>
                <p>Bacterie-geassisteerde fytoremediatie voor Cr in waterbodem en oevers.</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>

            <div class="rd-bodybox">
              <div class="rd-meta">
                <div class="rd-kv">
                  <div class="rd-k">Locatie & scope</div>
                  <div class="rd-v">Grote Calie Winkelsbroek</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Verontreiniging</div>
                  <div class="rd-v">Metalen (Cr) in waterbodem en oevers</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Rol & expertise</div>
                  <div class="rd-v">Ontwerp, implementatie & monitoring van bacterie-geassisteerde fytoremediatie.</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Highlights</div>
                  <div class="rd-v">
                    Inoculatie met Cr-reducerende bacteriën verhoogde Cr(III)-bioconcentratie in wortels van wilg, gras en boterbloem.
                    Chromaat-reductasegenen namen toe in de rhizosfeer, wat duurzame immobilisatie ondersteunt.
                  </div>
                </div>
              </div>

              <div class="rd-logos">
                <p class="label">Partners (logo’s)</p>
                <img src="{{ '/images/onderzoek/logos-narmena.jpg' | relative_url }}" alt="Partners LIFE NARMENA">
              </div>
            </div>
          </details>

        </div>
      </div>

      <!-- SECTION 2 -->
      <div class="rd-section">
        <h2>Academische projecten (UHasselt – 20%)</h2>
        <p class="lead">
          Lopende (en enkele afgeronde) projecten waarbij ik wetenschappelijke leiding of expertrol opneem via UHasselt/CMK.
        </p>

        <div class="rd-acc">

          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>PFAS fytoremediatie veldexperimenten — PLANTS project (KISS VZW, 2024–heden)</h3>
                <p>Identificatie van hennepcultivars met hoge PFOS-BCF; veldvalidatie in Vlaanderen.</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>

            <div class="rd-bodybox">
              <div class="rd-meta">
                <div class="rd-kv">
                  <div class="rd-k">Locatie & scope</div>
                  <div class="rd-v">Zwijndrecht & Kallo, Vlaanderen</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Verontreiniging</div>
                  <div class="rd-v">PFAS</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Rol & expertise</div>
                  <div class="rd-v">Wetenschappelijke leiding (expert via UHasselt/CMK).</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Highlights</div>
                  <div class="rd-v">
                    Hennepcultivars (o.a. Muka76) met PFOS-BCF 3–10× hoger dan alternatieve gewassen.
                    Jaarlijkse PFOS-reductie in bodem gerapporteerd rond 1–5% door fyto-extractie.
                  </div>
                </div>
              </div>

              <div class="rd-logos">
                <p class="label">Partners (logo’s)</p>
                <img src="{{ '/images/onderzoek/logos-plants.jpg' | relative_url }}" alt="Partners PLANTS">
              </div>
            </div>
          </details>

          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>MIBIREM — HORIZON-CL6-2021-CIRCBIO-01-07 (2022–2026)</h3>
                <p>Microbioom karakterisatie, isolatie, afbraaktesten en toolbox voor modellering van afbraakprocessen.</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>

            <div class="rd-bodybox">
              <div class="rd-meta">
                <div class="rd-kv">
                  <div class="rd-k">Locatie & scope</div>
                  <div class="rd-v">EU</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Verontreiniging</div>
                  <div class="rd-v">Petroleum koolwaterstoffen, cyanides, lindaan</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Rol & expertise</div>
                  <div class="rd-v">Wetenschappelijke leiding (WP2 via UHasselt/CMK).</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Highlights</div>
                  <div class="rd-v">
                    Microbioom karakterisatie, isolatie van bacteriën, afbraaktesten, consortia-samenstelling voor veldtoepassing,
                    en ontwikkeling bioinformatica toolbox voor modellering.
                  </div>
                </div>
              </div>

              <div class="rd-logos">
                <p class="label">Partners (logo’s)</p>
                <img src="{{ '/images/onderzoek/logos-mibirem.jpg' | relative_url }}" alt="Partners MIBIREM">
              </div>
            </div>
          </details>

          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>Fytostabilisatie met actieve kool (potproeven 3M)</h3>
                <p>Actieve kool (Rembind®) reduceert PFAS-opname in gewassen sterk.</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>

            <div class="rd-bodybox">
              <div class="rd-meta">
                <div class="rd-kv">
                  <div class="rd-k">Locatie & scope</div>
                  <div class="rd-v">UHasselt lab</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Verontreiniging</div>
                  <div class="rd-v">PFAS</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Rol & expertise</div>
                  <div class="rd-v">Wetenschappelijke leiding (expert via UHasselt/CMK).</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Highlights</div>
                  <div class="rd-v">
                    0,75% (w/w) actieve kool reduceerde totale PFAS-opname in spinazie met 94% (tot 0,61 μg/kg) en PFOS met 74%.
                    Concentraties onder EU-voedselveiligheidsdrempels.
                  </div>
                </div>
              </div>

              <div class="rd-logos">
                <p class="label">Partners (logo’s)</p>
                <img src="{{ '/images/onderzoek/logos-3m.jpg' | relative_url }}" alt="Partners 3M potproeven">
              </div>
            </div>
          </details>

          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>Constructed wetlands (haalbaarheidsstudie) — Blokkersdijk</h3>
                <p>Verwijderingsefficiënties van PFOS met geselecteerde grassoorten; onderzoek lopend met partners.</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>

            <div class="rd-bodybox">
              <div class="rd-meta">
                <div class="rd-kv">
                  <div class="rd-k">Locatie & scope</div>
                  <div class="rd-v">Blokkersdijk</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Verontreiniging</div>
                  <div class="rd-v">PFAS</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Rol & expertise</div>
                  <div class="rd-v">Wetenschappelijk partner (expert via UHasselt/CMK).</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Highlights</div>
                  <div class="rd-v">
                    Onderzoek naar PFOS-verwijdering met soorten zoals Phragmites en Juncus; verdere validatie in uitvoering.
                  </div>
                </div>
              </div>

              <div class="rd-logos">
                <p class="label">Partners (logo’s)</p>
                <img src="{{ '/images/onderzoek/logos-blokkersdijk.jpg' | relative_url }}" alt="Partners Blokkersdijk">
              </div>
            </div>
          </details>

        </div>
      </div>

      <!-- ARCHIVE -->
      <div class="rd-section">
        <h2>Archief (2019–2024)</h2>
        <p class="lead">
          Afgeronde of oudere projecten (samengevat). Voor detail: vraag gerust extra context of referenties.
        </p>

        <div class="rd-acc">

          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>INTERREG RESANAT (2019–2022) — microbe-ondersteunde fytopiles</h3>
                <p>Daling TPH & PAK16 tot ca. 40–70% na één groeiseizoen; multi-line-of-evidence onderbouwing.</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>
            <div class="rd-bodybox">
              <div class="rd-meta">
                <div class="rd-kv">
                  <div class="rd-k">Locatie & scope</div>
                  <div class="rd-v">De Lieve (baggerslib)</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Verontreiniging</div>
                  <div class="rd-v">Minerale olie (TPH), PAK’s</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Rol & expertise</div>
                  <div class="rd-v">Ontwerp & monitoring van microbe-ondersteunde fytopiles.</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Highlights</div>
                  <div class="rd-v">
                    Duidelijke toename van olie-afbrekende genen; o.a. 13C-gelabelde BACTRAPS binnen multi-line-of-evidence aanpak.
                  </div>
                </div>
              </div>

              <div class="rd-logos">
                <p class="label">Partners (logo’s)</p>
                <img src="{{ '/images/onderzoek/logos-resanat.jpg' | relative_url }}" alt="Partners RESANAT">
              </div>
            </div>
          </details>

          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>Pilootproef fytoremediatie VOCLs Roeselare (2018–2023)</h3>
                <p>Fy-tohydraulische aanpak: TCE & BTEX onder saneringsnormen bij afronding (maart 2023).</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>
            <div class="rd-bodybox">
              <div class="rd-meta">
                <div class="rd-kv">
                  <div class="rd-k">Locatie & scope</div>
                  <div class="rd-v">Roeselare pilootsite</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Verontreiniging</div>
                  <div class="rd-v">VOCl (TCE), BTEX</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Rol & expertise</div>
                  <div class="rd-v">Begeleiding bio2clean bij ontwerp & wetenschappelijke studie.</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Highlights</div>
                  <div class="rd-v">
                    Succesvolle toepassing van fytohydraulische aanpak; concentraties in grondwater onder saneringsnormen.
                  </div>
                </div>
              </div>

              <div class="rd-logos">
                <p class="label">Partners (logo’s)</p>
                <img src="{{ '/images/onderzoek/logos-roeselare.jpg' | relative_url }}" alt="Partners Roeselare">
              </div>
            </div>
          </details>

          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>OVAM Code van Goede Praktijk Fytoremediatie (2017–2019)</h3>
                <p>Vertaling van wetenschappelijke kennis naar Vlaamse richtlijn, in samenwerking met partners.</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>
            <div class="rd-bodybox">
              <div class="rd-meta">
                <div class="rd-kv">
                  <div class="rd-k">Locatie & scope</div>
                  <div class="rd-v">Vlaanderen (beleidskader)</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Verontreiniging</div>
                  <div class="rd-v">Diverse contaminanten</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Rol & expertise</div>
                  <div class="rd-v">Co-auteur (expert via UHasselt/CMK & bio2clean).</div>
                </div>
                <div class="rd-kv">
                  <div class="rd-k">Highlights</div>
                  <div class="rd-v">
                    Richtlijn om fytoremediatie wetenschappelijk correct én praktisch toepasbaar te maken (o.a. met Arcadis, Witteveen+Bos).
                  </div>
                </div>
              </div>

              <div class="rd-logos">
                <p class="label">Partners (logo’s)</p>
                <img src="{{ '/images/onderzoek/logos-ovam.jpg' | relative_url }}" alt="Partners OVAM">
              </div>
            </div>
          </details>

        </div>
      </div>

    </div>
  </section>
</div>
