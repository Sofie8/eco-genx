---
title: Projecten
layout: default
permalink: /projects/
---

<style>
  /* =========================================================
     Projects overview — Offshoots-style
     ========================================================= */

  /* full width page (zoals je service pages) */
  main{ max-width:none !important; padding:0 !important; overflow:visible !important; }
  main > *, main .content, main article, main .page, main .post{
    max-width:none !important; padding:0 !important; margin:0 !important; overflow:visible !important;
  }

  .projects-wrap{
    --max: 1200px;
    --pad: 1.25rem;
    --cream: var(--eco-cream, #f6f4ee);
    --green: var(--eco-dark, #0b3b2f);
    --green2: var(--eco-dark-2, #082a22);
    --ink: rgba(0,0,0,.86);
    --muted: rgba(0,0,0,.66);
    --line: rgba(0,0,0,.10);
  }

  .projects-hero{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    background: linear-gradient(180deg, rgba(11,59,47,.92), rgba(8,42,34,.92));
    color: rgba(255,255,255,.92);
    padding: 3.6rem 0 2.4rem;
  }
  .projects-hero__inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
    display: grid;
    grid-template-columns: 1.2fr .8fr;
    gap: 2rem;
    align-items: end;
  }

  .eyebrow{
    font-size: .86rem;
    letter-spacing: .10em;
    text-transform: uppercase;
    opacity: .8;
    margin-bottom: .6rem;
  }
  .projects-hero h1{
    margin: 0 0 .6rem;
    font-size: 3rem;
    line-height: 1.04;
    letter-spacing: .02em;
  }
  .projects-hero p{
    margin: 0;
    max-width: 72ch;
    line-height: 1.7;
    opacity: .92;
    font-size: 1.05rem;
  }

  .projects-hero__panel{
    border: 1px solid rgba(255,255,255,.16);
    border-radius: 18px;
    padding: 1.05rem 1.1rem;
    background: rgba(255,255,255,.06);
    box-shadow: 0 18px 44px rgba(0,0,0,.18);
  }

  /* filters */
  .filters{
    display:flex;
    flex-wrap:wrap;
    gap:.55rem;
    margin-top: .75rem;
  }
  .chip{
    appearance:none;
    border: 1px solid rgba(255,255,255,.18);
    background: rgba(255,255,255,.08);
    color: rgba(255,255,255,.92);
    padding: .45rem .75rem;
    border-radius: 999px;
    cursor:pointer;
    font: inherit;
    font-size: .92rem;
    transition: transform .12s ease, background .12s ease, border-color .12s ease;
    white-space: nowrap;
  }
  .chip:hover{ transform: translateY(-1px); background: rgba(255,255,255,.12); border-color: rgba(255,255,255,.26); }
  .chip.is-active{ background: rgba(75,191,122,.22); border-color: rgba(75,191,122,.55); }

  /* grid */
  .projects-body{
    background: var(--cream);
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;
    padding: 2.4rem 0 3.2rem;
    border-top: 1px solid rgba(0,0,0,.06);
  }
  .projects-body__inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
  }

  .grid{
    display:grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 1.25rem;
  }

  .card{
    background: rgba(255,255,255,.65);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    overflow: hidden;
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
    transition: transform .12s ease, box-shadow .12s ease;
    display:flex;
    flex-direction: column;
    min-height: 100%;
  }
  .card:hover{ transform: translateY(-2px); box-shadow: 0 18px 44px rgba(0,0,0,.10); }

  .card__media{
    aspect-ratio: 16 / 10;
    background: rgba(0,0,0,.06);
    position: relative;
    overflow: hidden;
  }
  .card__media img{
    width:100%;
    height:100%;
    object-fit: cover;
    display:block;
  }
  .badge{
    position:absolute;
    left: .85rem;
    bottom: .85rem;
    background: rgba(11,59,47,.92);
    color: rgba(255,255,255,.92);
    border: 1px solid rgba(255,255,255,.14);
    padding: .35rem .6rem;
    border-radius: 999px;
    font-size: .82rem;
    letter-spacing: .06em;
    text-transform: uppercase;
  }

  .card__body{
    padding: 1.05rem 1.05rem 1.1rem;
    display:flex;
    flex-direction: column;
    gap: .5rem;
  }
  .card__title{
    margin:0;
    font-size: 1.1rem;
    line-height: 1.25;
    color: var(--ink);
  }
  .meta{
    display:flex;
    gap:.65rem;
    flex-wrap:wrap;
    color: var(--muted);
    font-size: .92rem;
  }
  .card__desc{
    margin: .15rem 0 0;
    color: var(--muted);
    line-height: 1.65;
  }
  .card__link{
    margin-top: .55rem;
    align-self: flex-start;
    text-decoration: none;
    color: rgba(11,59,47,.92);
    font-weight: 600;
  }

  /* empty state */
  .empty{
    padding: 1.2rem;
    border-radius: 18px;
    border: 1px dashed rgba(0,0,0,.18);
    background: rgba(255,255,255,.55);
    color: var(--muted);
  }

  @media (max-width: 980px){
    .projects-hero__inner{ grid-template-columns: 1fr; }
    .projects-hero h1{ font-size: 2.2rem; }
    .grid{ grid-template-columns: 1fr; }
  }
</style>

<div class="projects-wrap">

  <section class="projects-hero">
    <div class="projects-hero__inner">
      <div>
        <div class="eyebrow">Eco-GenX · Projecten</div>
        <h1>Van analyse naar decision-ready resultaten</h1>
        <p>
          Een selectie van trajecten rond bodem-, water- en landschapsvraagstukken.
          Klik door voor context, aanpak en (later) resultaten/cases.
        </p>

        <div class="filters" id="projFilters">
          <button class="chip is-active" type="button" data-filter="all">Alles</button>
          <button class="chip" type="button" data-filter="restore">Restore</button>
          <button class="chip" type="button" data-filter="microproof">MicroProof</button>
          <button class="chip" type="button" data-filter="plantiq">PlantIQ</button>
        </div>
      </div>

      <div class="projects-hero__panel">
        <strong>Hoe ik projecten toon</strong>
        <div style="opacity:.92; margin-top:.35rem; line-height:1.6;">
          Korte omschrijving, scope en methodes. Later kan je hier makkelijk
          resultaten, foto’s, grafieken en referenties aan toevoegen.
        </div>
      </div>
    </div>
  </section>

  <section class="projects-body">
    <div class="projects-body__inner">

      {% assign items = site.projects | sort: "order" %}

      {% if items and items.size > 0 %}
        <div class="grid" id="projGrid">
          {% for p in items %}
            <a class="card"
               href="{{ p.url | relative_url }}"
               data-tags="{{ p.tags | join: ' ' | downcase }}">
              <div class="card__media">
                {% if p.cover %}
                  <img src="{{ p.cover | relative_url }}" alt="{{ p.title }}">
                {% endif %}
                {% if p.category %}
                  <span class="badge">{{ p.category }}</span>
                {% endif %}
              </div>

              <div class="card__body">
                <h3 class="card__title">{{ p.title }}</h3>
                <div class="meta">
                  {% if p.location %}<span>{{ p.location }}</span>{% endif %}
                  {% if p.year %}<span>· {{ p.year }}</span>{% endif %}
                </div>
                {% if p.excerpt %}
                  <p class="card__desc">{{ p.excerpt | strip_html | truncate: 140 }}</p>
                {% endif %}
                <span class="card__link">Bekijk project →</span>
              </div>
            </a>
          {% endfor %}
        </div>
      {% else %}
        <div class="empty">
          Nog geen projecten toegevoegd. Maak een map <code>_projects</code> en voeg er projectbestanden aan toe.
        </div>
      {% endif %}

    </div>
  </section>

</div>

<script>
  (function(){
    const filters = document.getElementById('projFilters');
    const grid = document.getElementById('projGrid');
    if(!filters || !grid) return;

    const chips = Array.from(filters.querySelectorAll('.chip'));
    const cards = Array.from(grid.querySelectorAll('.card'));

    function setActive(btn){
      chips.forEach(c => c.classList.remove('is-active'));
      btn.classList.add('is-active');
    }

    function apply(filter){
      cards.forEach(card => {
        const tags = (card.getAttribute('data-tags') || '').toLowerCase();
        const show = (filter === 'all') ? true : tags.includes(filter);
        card.style.display = show ? '' : 'none';
      });
    }

    filters.addEventListener('click', (e) => {
      const btn = e.target.closest('.chip');
      if(!btn) return;
      const filter = btn.getAttribute('data-filter');
      setActive(btn);
      apply(filter);
    });
  })();
</script>
