---
title: PlantIQ
layout: default
permalink: /plantiq/
redirect_from:
  - /PlantIQ/
  - /Plantiq/
nav:
  order: 3
  tooltip: PlantIQ
---

<style>
  /* ---------------------------------------------------------
     PlantIQ page — Full width sections (same look as MicroProof)
     Scoped to .svc-plantiq
     --------------------------------------------------------- */

  /* Force this page content full width (theme wraps markdown) */
  main{
    max-width: none !important;
    padding: 0 !important;
    overflow: visible !important;
  }
  main > *,
  main .content,
  main article,
  main .page,
  main .post{
    max-width: none !important;
    padding: 0 !important;
    margin: 0 !important;
    overflow: visible !important;
  }

  .svc-plantiq{
    --cream: #f6f4ee;
    --ink: rgba(0,0,0,.86);
    --muted: rgba(0,0,0,.68);
    --line: rgba(0,0,0,.08);
    --green: #0b3b2f;
  }

  /* Hero */
  .svc-plantiq .hero{
    position: relative;
    left: 50%;
    right: 50%;
    width: 100vw;
    margin-left: -50vw;
    margin-right: -50vw;

    background: linear-gradient(180deg, rgba(11,59,47,.92), rgba(8,42,34,.92));
    color: rgba(255,255,255,.92);
    padding: 4.6rem 0 3.2rem;
  }
  .svc-plantiq .hero-inner{
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1.25rem;
    display: grid;
    grid-template-columns: 1.2fr .8fr;
    gap: 2rem;
    align-items: end;
  }
  .svc-plantiq .eyebrow{
    font-size: .86rem;
    letter-spacing: .10em;
    text-transform: uppercase;
    opacity: .8;
    margin-bottom: .6rem;
  }
  .svc-plantiq h1{
    margin: 0 0 .6rem;
    font-size: 3rem;
    line-height: 1.04;
    letter-spacing: .02em;
  }
  .svc-plantiq .hero p{
    margin: 0;
    max-width: 72ch;
    line-height: 1.7;
    opacity: .92;
    font-size: 1.05rem;
  }

  .svc-plantiq .hero-card{
    border: 1px solid rgba(255,255,255,.16);
    border-radius: 18px;
    padding: 1.05rem 1.1rem;
    background: rgba(255,255,255,.06);
    box-shadow: 0 18px 44px rgba(0,0,0,.18);
  }
  .svc-plantiq .hero-card strong{ display:block; margin-bottom:.35rem; }
  .svc-plantiq .hero-card ul{
    margin:.45rem 0 0;
    padding-left: 1.1rem;
    opacity:.92;
  }

  /* Full width blocks */
  .svc-plantiq .block{
    position: relative;
    left: 50%;
    right: 50%;
    width: 100vw;
    margin-left: -50vw;
    margin-right: -50vw;

    display:grid;
    grid-template-columns: 1.15fr 1fr;
    min-height: 560px;
  }
  .svc-plantiq .block.reverse{
    grid-template-columns: 1fr 1.15fr;
  }

  .svc-plantiq .photo{
    position: relative;
    overflow:hidden;
  }
  .svc-plantiq .photo img{
    width:100%;
    height:100%;
    object-fit:cover;
    display:block;
  }

  .svc-plantiq .text{
    background: var(--cream);
    padding: 4.1rem 3.2rem;
    display:flex;
    flex-direction:column;
    justify-content:center;
    border-top: 1px solid var(--line);
    border-bottom: 1px solid var(--line);
  }

  .svc-plantiq .text h2{
    margin: 0 0 .75rem;
    font-size: 2.25rem;
    line-height: 1.08;
    color: var(--ink);
  }
  .svc-plantiq .lead{
    margin: 0 0 1.1rem;
    color: var(--muted);
    line-height: 1.75;
    max-width: 75ch;
    font-size: 1.03rem;
  }

  .svc-plantiq .key{
    margin-top: .6rem;
    padding-top: 1rem;
    border-top: 1px solid rgba(0,0,0,.10);
  }
  .svc-plantiq .key-title{
    font-weight: 700;
    letter-spacing: .02em;
    margin: 0 0 .5rem;
    color: var(--ink);
  }
  .svc-plantiq .key ul{
    margin: .2rem 0 0;
    padding-left: 1.1rem;
    color: var(--ink);
  }
  .svc-plantiq .key li{ margin: .35rem 0; }

  /* CTA */
  .svc-plantiq .cta{
    position: relative;
    left: 50%;
    right: 50%;
    width: 100vw;
    margin-left: -50vw;
    margin-right: -50vw;

    background: var(--green);
    color: rgba(255,255,255,.92);
    padding: 2.6rem 0;
  }
  .svc-plantiq .cta-inner{
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1.25rem;
    display:flex;
    flex-wrap:wrap;
    gap: 1rem 1.4rem;
    align-items:center;
    justify-content: space-between;
  }
  .svc-plantiq .cta h3{
    margin:0 0 .35rem;
    font-size: 1.6rem;
  }
  .svc-plantiq .cta p{
    margin:0;
    opacity:.9;
    max-width: 70ch;
  }
  .svc-plantiq .cta a{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    padding: .7rem 1rem;
    border-radius: 12px;
    border: 1px solid rgba(255,255,255,.22);
    background: rgba(255,255,255,.08);
    text-decoration:none;
    color: rgba(255,255,255,.92);
    white-space:nowrap;
  }
  .svc-plantiq .cta a:hover{ background: rgba(255,255,255,.12); }

  @media (max-width: 980px){
    .svc-plantiq .hero-inner{
      grid-template-columns: 1fr;
      align-items: start;
    }
    .svc-plantiq h1{ font-size: 2.2rem; }
    .svc-plantiq .block,
    .svc-plantiq .block.reverse{
      grid-template-columns: 1fr;
      min-height: auto;
    }
    .svc-plantiq .photo{ height: 340px; }
    .svc-plantiq .text{ padding: 2.2rem 1.25rem; }
    .svc-plantiq .text h2{ font-size: 1.85rem; }
  }
</style>

<div class="svc-plantiq">

  <!-- HERO -->
  <section class="hero">
    <div class="hero-inner">
      <div>
        <div class="eyebrow">Diensten · PlantIQ</div>
        <h1>Plantgenetica als beslissingskracht</h1>
        <p>
          PlantIQ helpt je om rassen/ouders doelgericht te kiezen en resistenties te stapelen —
          met genetische merkers die in de praktijk “decision-ready” output geven.
          Focus: koudeklimaat druiven en resistentie tegen valse en echte meeldauw.
        </p>
      </div>

      <div class="hero-card">
        <strong>Waar PlantIQ op focust</strong>
        <ul>
          <li>RhAmpSeq / SSR-seq merkers & haplotypes</li>
          <li>screening op meeldauw-resistentie (downy/powdery)</li>
          <li>advies voor selectie, kruising en validatie</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- BLOCK 1 -->
  <section class="block">
    <div class="photo">
      <img src="{{ '/images/plantiq-1.jpg' | relative_url }}" alt="Genetische screening en merkers">
    </div>

    <div class="text">
      <h2>1) Genetische screening die je keuzes versnelt</h2>
      <p class="lead">
        In veredeling en selectie wil je snel weten: <em>welke planten dragen de juiste resistenties</em>?
        PlantIQ zet merker-gebaseerde selectie in om seedlings, ouders of kandidaat-rassen vroeg te screenen,
        zodat je tijd en veldkosten bespaart.
      </p>

      <div class="key">
        <div class="key-title">Wat je eruit haalt</div>
        <ul>
          <li>snelle “go/no-go” op resistentie-loci</li>
          <li>minder afhankelijk van variabele veldinfectie</li>
          <li>duidelijke rapportering per plant/lot</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- BLOCK 2 -->
  <section class="block reverse">
    <div class="text">
      <h2>2) RhAmpSeq & SSR-seq voor meeldauw-resistentie</h2>
      <p class="lead">
        Voor druiven (zeker in koel klimaat) is resistentie tegen <strong>valse meeldauw</strong> en
        <strong>echte meeldauw</strong> vaak bepalend voor haalbare teelt met minder input.
        Met RhAmpSeq/SSR-seq kan je merkers robuust uitlezen en resistentie-haplotypes opvolgen.
      </p>
      <p class="lead">
        Praktisch: je krijgt een genetisch profiel dat je helpt om resistenties te identificeren,
        te combineren (stacking) en gericht door te selecteren naar volgende generaties.
      </p>

      <div class="key">
        <div class="key-title">Key methods</div>
        <ul>
          <li>RhAmpSeq (haplotype-gerichte merkers, stabiel over genetische achtergronden)</li>
          <li>SSR-seq / SSR genotypering (microsatellieten via sequencing)</li>
          <li>rapportering per merker/haplotype + interpretatie voor selectie</li>
        </ul>
      </div>
    </div>

    <div class="photo">
      <img src="{{ '/images/plantiq-2.jpg' | relative_url }}" alt="RhAmpSeq en SSR-seq merkers voor resistentie">
    </div>
  </section>

  <!-- BLOCK 3 -->
  <section class="block">
    <div class="photo">
      <img src="{{ '/images/plantiq-3.jpg' | relative_url }}" alt="Selectie, veredeling en decision support">
    </div>

    <div class="text">
      <h2>3) Van data naar veredeling: selectie & strategie</h2>
      <p class="lead">
        Genetische data is pas waardevol als je er beslissingen mee neemt. PlantIQ vertaalt resultaten naar:
        welke kruisingscombinaties kansrijk zijn, welke planten je behoudt, en waar je best valideert met fenotypering.
      </p>

      <div class="key">
        <div class="key-title">Typische deliverables</div>
        <ul>
          <li>selectielijst (behouden/uitselecteren) met motivatie</li>
          <li>advies voor resistentie-stacking en ouderskeuze</li>
          <li>validatieplan: veld/serre + eventueel koppeling met MicroProof (plant-microbioom)</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- CTA -->
  <section class="cta">
    <div class="cta-inner">
      <div>
        <h3>PlantIQ inzetten?</h3>
        <p>Stuur je doel (screening, ouders, resistentie-stacking), type materiaal en aantallen. Dan stel ik een merker-/analyseplan voor.</p>
      </div>
      <a href="{{ '/contact/' | relative_url }}">Contacteer mij →</a>
    </div>
  </section>

</div>
