---
title: Onderzoek
layout: default
permalink: /over/onderzoek/
---

<style>
  /* =========================================================
     Onderzoek — ISOdetect-ish: hero image + accordions
     Scope: .rdo
     ========================================================= */

  /* full width page */
  main{ max-width:none !important; padding:0 !important; overflow:visible !important; }
  main > *, main .content, main article, main .page, main .post{
    max-width:none !important; padding:0 !important; margin:0 !important; overflow:visible !important;
  }

  .rdo{
    --max: 1200px;
    --pad: 1.25rem;

    --cream: var(--eco-cream, #f6f4ee);
    --green: var(--eco-dark, #0b3b2f);
    --green2: var(--eco-dark-2, #082a22);

    --ink: rgba(0,0,0,.86);
    --muted: rgba(0,0,0,.66);
    --line: rgba(0,0,0,.10);
  }

  /* HERO full width */
  .rdo-hero{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    min-height: 420px;
    background: #0b3b2f;
    background-size: cover;
    background-position: center;
    border-bottom: 1px solid rgba(0,0,0,.08);
  }
  .rdo-hero::before{
    content:"";
    position:absolute; inset:0;
    background: linear-gradient(90deg,
      rgba(8,42,34,.86) 0%,
      rgba(8,42,34,.62) 45%,
      rgba(8,42,34,.22) 100%);
  }

  .rdo-hero .inner{
    position: relative;
    max-width: var(--max);
    margin: 0 auto;
    padding: 3.2rem var(--pad);
    color: rgba(255,255,255,.92);

    display:grid;
    grid-template-columns: 1.15fr .85fr;
    gap: 2rem;
    align-items: end;
  }

  .rdo-eyebrow{
    font-size: .86rem;
    letter-spacing: .10em;
    text-transform: uppercase;
    opacity: .86;
    margin-bottom: .6rem;
  }
  .rdo h1{
    margin: 0 0 .6rem;
    font-size: 3rem;
    line-height: 1.04;
    letter-spacing: .02em;
  }
  .rdo-hero p{
    margin: 0;
    max-width: 75ch;
    line-height: 1.7;
    opacity: .92;
    font-size: 1.05rem;
  }

  .rdo-hero .panel{
    border: 1px solid rgba(255,255,255,.16);
    border-radius: 18px;
    padding: 1.05rem 1.1rem;
    background: rgba(255,255,255,.06);
    box-shadow: 0 18px 44px rgba(0,0,0,.18);
  }
  .rdo-hero .panel strong{ display:block; margin-bottom:.35rem; }
  .rdo-hero .panel ul{ margin:.45rem 0 0; padding-left: 1.1rem; opacity:.92; }
  .rdo-hero .panel li{ margin:.35rem 0; }

  /* SECTION base */
  .rdo-body{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    background: var(--cream);
    padding: 2.6rem 0 3.2rem;
    border-top: 1px solid rgba(0,0,0,.06);
  }
  .rdo-body .inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
  }

  .rdo h2{
    margin: 0 0 .65rem;
    font-size: 1.8rem;
    line-height: 1.2;
    color: var(--ink);
  }
  .rdo .intro{
    margin: 0 0 1.2rem;
    max-width: 82ch;
    color: var(--muted);
    line-height: 1.75;
  }

  /* ACCORDIONS */
  .acc-group{ margin: 1.2rem 0 2.2rem; }

  .acc{
    background: rgba(255,255,255,.62);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    overflow: hidden;
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
    margin-bottom: .85rem;
  }

  .acc summary{
    list-style: none;
    cursor: pointer;
    padding: 1.05rem 1.15rem;
    display:flex;
    align-items:flex-start;
    justify-content: space-between;
    gap: 1rem;
  }
  .acc summary::-webkit-details-marker{ display:none; }

  .acc .sum-left{
    display:flex;
    flex-direction: column;
    gap: .25rem;
  }
  .acc .sum-title{
    font-weight: 750;
    color: var(--ink);
    font-size: 1.05rem;
    line-height: 1.25;
  }
  .acc .sum-sub{
    color: var(--muted);
    line-height: 1.55;
  }

  /* plus icon */
  .acc .plus{
    flex: 0 0 auto;
    width: 28px;
    height: 28px;
    border-radius: 999px;
    border: 1px solid rgba(0,0,0,.18);
    display:grid;
    place-items:center;
    color: rgba(0,0,0,.66);
    margin-top: .15rem;
    background: rgba(255,255,255,.55);
    transition: transform .15s ease;
  }
  details[open] .plus{ transform: rotate(45deg); }

  .acc .body{
    padding: 0 1.15rem 1.15rem;
    color: rgba(0,0,0,.74);
    line-height: 1.75;
  }

  .meta{
    display:flex;
    flex-wrap:wrap;
    gap:.5rem;
    margin-top: .75rem;
  }
  .badge{
    font-size: .82rem;
    padding: .28rem .55rem;
    border-radius: 999px;
    border: 1px solid rgba(0,0,0,.12);
    background: rgba(0,0,0,.04);
    color: rgba(0,0,0,.72);
  }
  .badge.green{
    border-color: rgba(75,191,122,.45);
    background: rgba(75,191,122,.14);
    color: rgba(11,59,47,.92);
  }

  /* ARCHIEF: jaarblokken (HPC-ish) */
  .year{
    border-top: 1px solid rgba(0,0,0,.12);
    padding-top: 1.2rem;
    margin-top: 1.2rem;
  }
  .year h3{
    margin: 0 0 .65rem;
    font-size: 1.15rem;
    letter-spacing: .06em;
    text-transform: uppercase;
    opacity: .82;
  }

  /* responsive */
  @media (max-width: 980px){
    .rdo-hero .inner{ grid-template-columns: 1fr; padding: 2.4rem var(--pad); }
    .rdo h1{ font-size: 2.2rem; }
  }
</style>

<div class="rdo">

  <!-- HERO: 1 figuur over volle breedte -->
  <section class="rdo-hero"
    style="background-image:url('{{ '/images/research/research-hero.jpg' | relative_url }}')">
    <div class="inner">
      <div>
        <div class="rdo-eyebrow">Eco-GenX · Onderzoek & ontwikkeling</div>
        <h1>Van wetenschap naar terrein</h1>
        <p>
          Ik ontwikkel en test meetbare innovaties rond bodem-, water- en PFAS-herstel:
          nature-based ontwerpen, evidence-plannen en monitoring die decision-ready antwoorden opleveren.
        </p>
      </div>

      <div class="panel">
        <strong>Hoe ik dit toon</strong>
        <ul>
          <li>lopende projecten (Eco-GenX)</li>
          <li>academische projecten (UHasselt, 20%)</li>
          <li>archief per jaar</li>
        </ul>
      </div>
    </div>
  </section>

  <section class="rdo-body">
    <div class="inner">

      <!-- 1) ECO-GENX -->
      <h2>Lopende projecten — Eco-GenX</h2>
      <p class="intro">
        Projecten waarbij ik betrokken ben via Eco-GenX / vennootschap (advies, ontwerp, monitoring, proof-of-impact).
      </p>

      <div class="acc-group">

        <!-- Barebeek (toegevoegd) -->
        <details class="acc">
          <summary>
            <div class="sum-left">
              <div class="sum-title">Barebeek (Zemst) — PFAS piloot & demonstratie</div>
              <div class="sum-sub">
                Nature-based ingrepen om PFAS-vang efficiëntie in de sedimentvang te verhogen, met multi-line-of-evidence monitoring.
              </div>
            </div>
            <div class="plus">+</div>
          </summary>
          <div class="body">
            <p>
              In-situ aanpak met o.a. floating treatment wetlands en oeverbeplanting (en waar passend reactief substraat),
              gekoppeld aan monitoring van concentraties én fluxen (richting grondwater/oppervlaktewater) om effectiviteit aantoonbaar te maken.
            </p>
            <div class="meta">
              <span class="badge green">Eco-GenX</span>
              <span class="badge">PFAS</span>
              <span class="badge">wetlands</span>
              <span class="badge">monitoring</span>
            </div>
          </div>
        </details>

        <!-- voorbeeld placeholder -->
        <details class="acc">
          <summary>
            <div class="sum-left">
              <div class="sum-title">PFAS RESOLVE — evidence & monitoring (voorbeeld)</div>
              <div class="sum-sub">Korte uitleg wat jij wil tonen (later aanvullen).</div>
            </div>
            <div class="plus">+</div>
          </summary>
          <div class="body">
            <p>Vul hier later details aan: doel, aanpak, deliverables, partners, status.</p>
            <div class="meta">
              <span class="badge green">Eco-GenX</span>
              <span class="badge">PFAS</span>
              <span class="badge">evidence</span>
            </div>
          </div>
        </details>

      </div>

      <!-- 2) UHASSELT -->
      <h2>Lopende academische projecten — UHasselt (20%)</h2>
      <p class="intro">
        Projecten waarbij ik betrokken ben via mijn academische aanstelling (onderzoek, methodiek, publicatie/validatie).
      </p>

      <div class="acc-group">

        <details class="acc">
          <summary>
            <div class="sum-left">
              <div class="sum-title">PFAS fytoremediatie — veldexperimenten & mechanistische inzichten</div>
              <div class="sum-sub">Voorbeeldstructuur: voeg je eigen titels en 2–3 lijnen toe.</div>
            </div>
            <div class="plus">+</div>
          </summary>
          <div class="body">
            <p>Vul hier je academische projecten aan (doel, aanpak, rol, output).</p>
            <div class="meta">
              <span class="badge">UHasselt</span>
              <span class="badge">fytoremediatie</span>
              <span class="badge">PFAS</span>
            </div>
          </div>
        </details>

      </div>

      <!-- 3) ARCHIEF -->
      <h2>Archief</h2>
      <p class="intro">
        Afgeronde of oudere projecten, per jaar. Gebruik badges om Eco-GenX vs UHasselt duidelijk te houden.
      </p>

      <div class="year">
        <h3>2024</h3>

        <details class="acc">
          <summary>
            <div class="sum-left">
              <div class="sum-title">Titel archiefproject — korte omschrijving</div>
              <div class="sum-sub">1 zin: waarom relevant, wat werd gedaan.</div>
            </div>
            <div class="plus">+</div>
          </summary>
          <div class="body">
            <p>Detail (2–5 zinnen), eventueel link naar project/case/paper.</p>
            <div class="meta">
              <span class="badge green">Eco-GenX</span>
              <span class="badge">tag</span>
            </div>
          </div>
        </details>

      </div>

      <div class="year">
        <h3>2023</h3>

        <details class="acc">
          <summary>
            <div class="sum-left">
              <div class="sum-title">Titel archiefproject — korte omschrijving</div>
              <div class="sum-sub">1 zin: resultaat/impact.</div>
            </div>
            <div class="plus">+</div>
          </summary>
          <div class="body">
            <p>Detailtekst.</p>
            <div class="meta">
              <span class="badge">UHasselt</span>
              <span class="badge">tag</span>
            </div>
          </div>
        </details>

      </div>

    </div>
  </section>

</div>
