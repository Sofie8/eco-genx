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
     ONDERZOEK — Eco-GenX style (hero + accordions)
     Scoped: .rd
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

  /* ---------- HERO (zoals artikels: niet te hoog) ---------- */
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
    max-width: 82ch;
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

  /* ---------- INTRO BLOCK (2 columns like iso page) ---------- */
  .rd-intro{
    display:grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    align-items:start;
    margin-bottom: 2rem;
  }
  .rd-intro h2{
    margin: 0 0 .6rem;
    font-size: 1.65rem;
    line-height: 1.2;
    color: var(--ink);
  }
  .rd-intro p{
    margin: 0;
    color: rgba(0,0,0,.74);
    line-height: 1.75;
    max-width: 85ch;
    text-align:left !important;
  }

  .rd-note{
    background: rgba(255,255,255,.62);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    overflow:hidden;
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
  }
  .rd-note .pad{ padding: 1.25rem 1.35rem; }
  .rd-note strong{ display:block; margin-bottom:.35rem; }

  /* ---------- SECTION HEAD ---------- */
  .rd-section{
    margin: 0 0 2.0rem;
  }
  .rd-section h2{
    margin: 0 0 .6rem;
    font-size: 1.85rem;
    line-height: 1.2;
    color: var(--ink);
  }
  .rd-section p{
    margin: 0 0 1.1rem;
    color: rgba(0,0,0,.74);
    line-height: 1.75;
    max-width: 92ch;
    text-align:left !important;
  }

  /* ---------- Accordion list (FIX alignment + centered content) ---------- */
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
    width: 100%;
  }

  /* summary = centered content (no weird right packing) */
  summary.rd-sum{
    list-style: none;
    cursor: pointer;

    display:grid !important;
    grid-template-columns: 40px minmax(0, 1fr) 42px;
    gap: 1rem;
    align-items: start;

    width: 100%;
    padding: 1.05rem 1.15rem;
    background: rgba(0,0,0,.04);

    place-content: stretch !important;
    justify-content: stretch !important;
    justify-items: stretch !important;

    max-width: 980px;
    margin: 0 auto;

    text-align:left !important;
  }

  summary.rd-sum::-webkit-details-marker{ display:none; }
  summary.rd-sum::marker{ content:""; }
  summary.rd-sum::before{ content:none !important; }

  .rd-sum > div{ min-width: 0; }

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
    text-align:left !important;
  }
  .rd-sum p{
    margin: 0;
    color: rgba(0,0,0,.70);
    line-height: 1.6;
    text-align:left !important;
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
    font-size: 1.35rem;
    line-height: 1;
    user-select: none;
  }

  /* default closed => show +  */
  details.rd-item:not([open]) .rd-plus::before{ content:"+"; }
  /* open => show – */
  details.rd-item[open] .rd-plus::before{ content:"–"; }

  details.rd-item[open] .rd-chev{
    transform: rotate(90deg);
    transition: transform .15s ease;
  }

  .rd-bodybox{
    padding: 1.05rem 1.15rem 1.15rem;
    background: rgba(255,255,255,.55);
  }

  /* center expanded content too */
  .rd-bodybox > *{
    max-width: 980px;
    margin-left: auto;
    margin-right: auto;
    text-align:left !important;
  }

  /* per project: logo group image */
  .rd-logos{
    margin-top: .85rem;
    padding-top: .85rem;
    border-top: 1px solid rgba(0,0,0,.10);
  }
  .rd-logos img{
    width: 100%;
    max-width: 980px;
    height: auto;
    display:block;
    border-radius: 14px;
    border: 1px solid rgba(0,0,0,.08);
    background: rgba(255,255,255,.6);
  }
  .rd-logos .hint{
    margin-top: .45rem;
    color: rgba(0,0,0,.62);
    font-size: .95rem;
    line-height: 1.6;
  }

  /* ---------- Responsive ---------- */
  @media (max-width: 980px){
    .rd-hero{ height: 240px; }
    .rd-hero__inner{ padding: 1.2rem 0 1rem; }
    .rd-title{ font-size: 1.95rem; }
    .rd-intro{ grid-template-columns: 1fr; }
  }
</style>

<div class="rd">

  <!-- HERO -->
  <section class="rd-hero" aria-label="Onderzoek en ontwikkeling">
    <img src="{{ '/images/onderzoek-hero.jpg' | relative_url }}" alt="Onderzoek en ontwikkeling">
    <div class="rd-hero__inner">
      <div class="inner">
        <div class="rd-eyebrow">Eco-GenX · Onderzoek & ontwikkeling</div>
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

      <!-- INTRO BLOCK (UHasselt postdoc context) -->
      <div class="rd-intro">
        <div>
          <h2>Onderzoek als motor</h2>
          <p>
            Eco-GenX is praktijkgericht: ontwerpen, testen en onderbouwen op terrein.
            Tegelijk blijf ik als postdoc (20% aanstelling) bij UHasselt nauw betrokken bij
            fundamentele en methodologische ontwikkeling (plant–microbe interacties, bewijsvoering, data-interpretatie).
            Dat houdt de aanpak scherp en vertaalt nieuwe inzichten sneller naar toepasbare oplossingen.
          </p>
        </div>
        <div class="rd-note">
          <div class="pad">
            <strong>Hoe ik dit toon</strong>
            <p style="margin:0; color: rgba(0,0,0,.72); line-height:1.7;">
              Lopende projecten (Eco-GenX) en een compact archief (2019–2024).
              Per project kan je een korte omschrijving uitbreiden en logo’s/partners tonen via één afbeelding.
            </p>
          </div>
        </div>
      </div>

      <!-- SECTION: Eco-GenX current -->
      <div class="rd-section">
        <h2>Huidige onderzoek- & ontwikkelingsprojecten (Eco-GenX)</h2>
        <p>
          Projecten waarbij ik betrokken ben via Eco-GenX/vennootschap (advies, ontwerp, monitoring, proof-of-impact).
          Klik open voor details en voeg per project een logo-beeld toe.
        </p>

        <div class="rd-acc">

          <!-- Barebeek -->
          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>Barebeek (Zemst) — PFAS piloot & demonstratie (2025–2028)</h3>
                <p>Nature-based ingrepen om PFAS-vang efficiënter te maken in sedimentvang, met multi-line-of-evidence monitoring.</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>

            <div class="rd-bodybox">
              <p>
                Pilootproject (VMM) rond innovatieve in-situ sanering om verspreiding van PFAS via sediment en oppervlaktewater te reduceren.
                Traject met nulmeting → ontwerp → real-scale implementatie → effectmonitoring (incl. concentraties én fluxen richting grondwater/oppervlaktewater, iFLUX).
              </p>
              <p>
                Rol: expert plant–microbe interacties voor PFAS sorptie/extractie; haalbaarheidsstudie, experimenteel design en data-interpretatie
                voor constructed floating wetlands en oeverbeplanting (eventueel met reactief substraat).
              </p>

              <div class="rd-logos">
                <!-- upload 1 samengestelde logo-afbeelding voor dit project -->
                <img src="{{ '/images/logos/barebeek-logos.png' | relative_url }}" alt="Partners & logo's — Barebeek PFAS">
                <div class="hint">Upload hier één logo-afbeelding (bv. VMM, UHasselt, iFLUX, partners) als <code>/images/logos/barebeek-logos.png</code>.</div>
              </div>
            </div>
          </details>

          <!-- PFAS RESOLVE -->
          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>Interreg PFAS RESOLVE (2024–2027)</h3>
                <p>Veldpilots met plant-gebaseerde staalname + draagbare biosensor als snel alternatief voor labanalyses.</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>

            <div class="rd-bodybox">
              <p>
                Grensoverschrijdende regio Maas-Rijn (PFAS incl. PFOS, PFOA, GenX).
                Rol: verantwoordelijk voor phyto-screening en veldpilots (in opdracht van bio2clean).
              </p>
              <p>
                Opzet van veldpilots waarin plant-gebaseerde staalname wordt gecombineerd met een nieuwe draagbare biosensor.
                Doel: snel en kostenefficiënt alternatief voor grootschalige kartering en monitoring.
              </p>

              <div class="rd-logos">
                <img src="{{ '/images/logos/pfas-resolve-logos.png' | relative_url }}" alt="Partners & logo's — PFAS RESOLVE">
                <div class="hint">Zet hier je projectlogo’s als één bestand: <code>/images/logos/pfas-resolve-logos.png</code>.</div>
              </div>
            </div>
          </details>

          <!-- LIFE NARMENA -->
          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>LIFE NARMENA (2020–2026)</h3>
                <p>Bacterie-geassisteerde fytoremediatie voor Cr in waterbodem en oevers (Grote Calie – Winkelsbroek).</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>

            <div class="rd-bodybox">
              <p>
                Ontwerp, implementatie & monitoring van bacterie-geassisteerde fytoremediatie.
                Inoculatie met Cr-reducerende bacteriën verhoogde Cr(III)-bioconcentratie in wortels (wilg, gras, boterbloem).
              </p>
              <p>
                Toename van chromaat-reductasegenen in de rhizosfeer ondersteunt duurzame immobilisatie van chroom.
              </p>

              <div class="rd-logos">
                <img src="{{ '/images/logos/narmena-logos.png' | relative_url }}" alt="Partners & logo's — LIFE NARMENA">
                <div class="hint">Zet hier je projectlogo’s als één bestand: <code>/images/logos/narmena-logos.png</code>.</div>
              </div>
            </div>
          </details>

        </div>
      </div>

      <!-- SECTION: Archive -->
      <div class="rd-section">
        <h2>Archief (2019–2024)</h2>
        <p>
          Afgeronde of oudere projecten, gebundeld. Klik open voor context en kernresultaten.
        </p>

        <div class="rd-acc">

          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>PFAS fytoremediatie veldexperimenten — PLANTS project KISS VZW (2024–heden)</h3>
                <p>Identificatie van hennepcultivars met hoge BCF voor PFOS; jaarlijkse PFOS-reducties 1–5% (fyto-extractie).</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>
            <div class="rd-bodybox">
              <p>
                Locatie: Zwijndrecht & Kallo (Vlaanderen). Wetenschappelijke leiding (expertise via UHasselt/CMK).
                Cultivarselectie (o.a. Muka76) met BCF voor PFOS ~3–10× hoger dan alternatieve gewassen.
              </p>
              <div class="rd-logos">
                <img src="{{ '/images/logos/plants-kiss-logos.png' | relative_url }}" alt="Partners & logo's — PLANTS / KISS">
              </div>
            </div>
          </details>

          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>MIBIREM — HORIZON-CL6 (2022–2026)</h3>
                <p>Microbioom-karakterisatie, isolaties, afbraaktesten en toolbox voor modellering van afbraakprocessen.</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>
            <div class="rd-bodybox">
              <p>
                Contaminanten: petroleum koolwaterstoffen, cyanides, lindaan. Wetenschappelijke leiding (WP2 via UHasselt/CMK).
                Van isolatie en consortia tot veld-toepassing (bacterie-gestimuleerde fytoremediatie) en bioinformatica.
              </p>
              <div class="rd-logos">
                <img src="{{ '/images/logos/mibirem-logos.png' | relative_url }}" alt="Partners & logo's — MIBIREM">
              </div>
            </div>
          </details>

          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>INTERREG RESANAT (2019–2022)</h3>
                <p>Microbe-ondersteunde fytopiles; daling TPH/PAK16 ca. 40–70% na één groeiseizoen (multi-evidence).</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>
            <div class="rd-bodybox">
              <p>
                Locatie: De Lieve (baggerslib). Ontwerp & monitoring van microbe-ondersteunde fytopiles.
                Onderbouwing o.a. via toename olie-afbrekende genen en 13C-gelabelde BACTRAPS.
              </p>
              <div class="rd-logos">
                <img src="{{ '/images/logos/resanat-logos.png' | relative_url }}" alt="Partners & logo's — RESANAT">
              </div>
            </div>
          </details>

          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>Pilootproef fytoremediatie VOCLs Roeselare (2018–2023)</h3>
                <p>Fytohydraulische aanpak; TCE/BTEX daalden tot onder saneringsnormen (afronding maart 2023).</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>
            <div class="rd-bodybox">
              <p>
                Begeleiding bio2clean bij ontwerp & wetenschappelijke studie. Succesvolle toepassing fytohydraulische aanpak.
              </p>
              <div class="rd-logos">
                <img src="{{ '/images/logos/roeselare-logos.png' | relative_url }}" alt="Partners & logo's — Roeselare">
              </div>
            </div>
          </details>

          <details class="rd-item">
            <summary class="rd-sum">
              <div class="rd-chev">›</div>
              <div>
                <h3>OVAM Code van Goede Praktijk Fytoremediatie (2017–2019)</h3>
                <p>Vertaling van wetenschap naar praktijkrichtlijn (co-auteur; samen met o.a. Arcadis, Witteveen+Bos).</p>
              </div>
              <div class="rd-plus" aria-hidden="true"></div>
            </summary>
            <div class="rd-bodybox">
              <p>
                Beleidskader Vlaanderen. Mede-opsteller van de Vlaamse richtlijn om fytoremediatie wetenschappelijk correct én toepasbaar te maken.
              </p>
              <div class="rd-logos">
                <img src="{{ '/images/logos/ovam-code-logos.png' | relative_url }}" alt="Partners & logo's — OVAM code">
              </div>
            </div>
          </details>

        </div>
      </div>

    </div>
  </section>

</div>

<script>
  // Force all accordions closed by default (so you see +)
  document.addEventListener('DOMContentLoaded', function(){
    document.querySelectorAll('details.rd-item[open]').forEach(d => d.removeAttribute('open'));
  });
</script>
