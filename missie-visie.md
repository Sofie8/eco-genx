---
title: Missie & visie
layout: default
permalink: /over/missie-visie/
---

<style>
  /* =========================================
     Force this page to be full width
     (your template wraps markdown in extra containers)
     ========================================= */
  main{
    max-width: none !important;
    padding: 0 !important;
    overflow: visible !important;
  }
  /* common wrappers in lab website templates / markdown layouts */
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

  /* =========================================
     Missie/Visie layout (Biologic vibe)
     ========================================= */
  .mv-block{
    display:grid;
    grid-template-columns: 1.15fr 1fr;
    min-height: 560px;
  }

  .mv-photo{
    position: relative;
    overflow: hidden;
  }
  .mv-photo img{
    width:100%;
    height:100%;
    object-fit: cover;
    display:block;
  }

  .mv-text{
    background: #f6f4ee;
    padding: 4.2rem 3.2rem;
    display:flex;
    flex-direction: column;
    justify-content: center;
    border-top: 1px solid rgba(0,0,0,.06);
    border-bottom: 1px solid rgba(0,0,0,.06);
  }

  .eyebrow{
    font-size: .86rem;
    letter-spacing: .08em;
    text-transform: uppercase;
    opacity: .7;
    margin-bottom: .55rem;
  }

  .mv-text h1, .mv-text h2{
    margin: 0 0 .85rem;
    font-size: 2.55rem;
    line-height: 1.06;
    letter-spacing: .02em;
  }

  .mv-text p{
    margin: 0 0 1rem;
    font-size: 1.06rem;
    line-height: 1.75;
    max-width: 72ch;
    opacity: .92;
  }

  .mv-block.reverse{
    grid-template-columns: 1fr 1.15fr;
  }

  @media (max-width: 980px){
    .mv-block, .mv-block.reverse{
      grid-template-columns: 1fr;
      min-height: auto;
    }
    .mv-photo{ height: 360px; }
    .mv-text{ padding: 2.2rem 1.25rem; }
    .mv-text h1, .mv-text h2{ font-size: 2rem; }
  }
</style>

<!-- MISSIE -->
<section class="mv-block">
  <div class="mv-photo">
    <img src="{{ '/images/about-mission-1.jpg' | relative_url }}" alt="Eco-GenX missie — natuur-gebaseerde oplossingen">
  </div>

  <div class="mv-text">
    <div class="eyebrow">Missie</div>
    <h1>Data-gedreven, natuur-gebaseerde oplossingen.</h1>
    <p>
      Eco-GenX is dé partner voor data-gedreven, natuur-gebaseerde oplossingen in bodemherstel en landbouw.
      Wij combineren ecologische expertise met genetische precisie om meetbaar bewijs te leveren,
      risico’s te beheren en uw projectdoelen te realiseren.
    </p>
    <p style="opacity:.78; margin:0;">
      Resultaten waar je beslissingen op kan nemen — van analyse tot monitoring en bijsturing.
    </p>
  </div>
</section>

<!-- VISIE -->
<section class="mv-block reverse">
  <div class="mv-text">
    <div class="eyebrow">Visie</div>
    <h2>De natuur als meest efficiënte technologie.</h2>
    <p>
      Wij werken aan een toekomst waarin de natuur de meest efficiënte technologie is.
      Door biologische processen intelligent te sturen met data, bieden we zekerheid bij complexe milieu- en landbouwprojecten.
      Zo maken we landschappen veerkrachtiger, productiever en schoner.
    </p>
    <p style="opacity:.78; margin:0;">
      Niet alleen inzetten — maar ook begrijpen, sturen en meten.
    </p>
  </div>

  <div class="mv-photo">
    <img src="{{ '/images/about-mission-2.jpg' | relative_url }}" alt="Eco-GenX visie — veerkrachtige landschappen">
  </div>
</section>
