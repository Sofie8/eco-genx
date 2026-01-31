---
title: Over Eco-GenX
layout: default
permalink: /over/
redirect_to: /over/wie-ben-ik/
nav:
  order: 2
  tooltip: Over Eco-GenX
---

<style>
  .over-wrap{
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1.25rem;
    box-sizing: border-box;
  }
  .over-hero{
    margin: 1.4rem 0 1.8rem;
  }
  .eyebrow{
    font-size: .86rem;
    letter-spacing: .08em;
    text-transform: uppercase;
    opacity: .7;
    margin-bottom: .5rem;
  }
  .over-hero h1{
    margin: 0 0 .7rem;
    font-size: 2.2rem;
    line-height: 1.1;
  }
  .lead{
    max-width: 78ch;
    opacity: .86;
    line-height: 1.7;
  }

  .grid{
    display:grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 1.2rem;
    margin: 1.4rem 0 2.2rem;
  }
  .card{
    background:#fff;
    border:1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    padding: 1.25rem 1.25rem 1.1rem;
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
    text-decoration:none;
    color: inherit;
    transition: transform .12s ease, box-shadow .12s ease;
  }
  .card:hover{
    transform: translateY(-1px);
    box-shadow: 0 18px 44px rgba(0,0,0,.10);
  }
  .card h3{ margin: 0 0 .45rem; }
  .card p{ margin: 0; opacity: .82; }
</style>

<div class="over-wrap">
  <section class="over-hero">
    <div class="eyebrow">Over Eco-GenX</div>
    <h1>Engineering nature, met meetbaar bewijs.</h1>
    <p class="lead">
      Eco-GenX helpt organisaties om milieuvraagstukken aan te pakken met de best beschikbare wetenschap —
      vertaald naar keuzes en acties die werken in de praktijk.
    </p>
  </section>

  <section class="grid">
    <a class="card" href="{{ '/over/wie-ben-ik/' | relative_url }}">
      <h3>Wie ben ik?</h3>
      <p>Mijn achtergrond, drijfveer en waarom ik Eco-GenX startte.</p>
    </a>

    <a class="card" href="{{ '/over/missie-visie/' | relative_url }}">
      <h3>Missie & visie</h3>
      <p>Waar Eco-GenX voor staat en waar we naartoe willen.</p>
    </a>

    <a class="card" href="{{ '/over/voor-wie/' | relative_url }}">
      <h3>Voor wie</h3>
      <p>Voor welke organisaties en projecten Eco-GenX het meeste waarde toevoegt.</p>
    </a>

    <a class="card" href="{{ '/over/onderzoek/' | relative_url }}">
      <h3>Onderzoek</h3>
      <p>De wetenschappelijke basis: microbiële processen, DNA/eDNA en fytotechnologie.</p>
    </a>

    <a class="card" href="{{ '/over/communicatie/' | relative_url }}">
      <h3>Communicatie</h3>
      <p>Artikels, lezingen, workshops en kennisdeling.</p>
    </a>
  </section>
</div>
