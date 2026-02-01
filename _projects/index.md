---
title: Projecten
layout: default
permalink: /projects/
---

<style>
  /* Hide the default page title that the theme/layout injects */
.page-title,
.page-header,
.page-header h1,
h1.page-title,
main > h1:first-child{
  display:none !important;
}

  /* =========================================================
     PROJECTS — Filter bar + uniform tile grid (Offshoots-like)
     Fixes:
     - geen "Projecten" hero/titelblok
     - tiles altijd gelijke hoogte (cover crop)
     ========================================================= */

  /* full width page */
  main{ max-width:none !important; padding:0 !important; overflow:visible !important; }
  main > *, main .content, main article, main .page, main .post{
    max-width:none !important; padding:0 !important; margin:0 !important; overflow:visible !important;
  }

  .projects-page{
    --max: 1200px;
    --pad: 1.25rem;
    --cream: var(--eco-cream, #f6f4ee);
    --ink: rgba(0,0,0,.86);
    --muted: rgba(0,0,0,.62);
    --line: rgba(0,0,0,.10);
    --chip: #d8d8d8;
    --chip-active: #3a3a3a;
  }

  /* TOP FILTERS (zoals je screenshot) */
  .projects-top{
    background: #fff;
    border-bottom: 1px solid var(--line);
    padding: 1.2rem 0 .9rem;
  }
  .projects-top__inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
  }

  .filters-title{
    font-size: .95rem;
    letter-spacing: .08em;
    text-transform: uppercase;
    opacity: .8;
    margin: 0 0 .65rem;
  }

  .chipbar{
    display:flex;
    flex-wrap:wrap;
    gap: .55rem .55rem;
  }
  .chip{
    appearance:none;
    border: 0;
    background: var(--chip);
    color: rgba(0,0,0,.78);
    padding: .5rem .7rem;
    border-radius: 0;
    cursor:pointer;
    font: inherit;
    font-size: .95rem;
    line-height: 1.2;
    transition: filter .12s ease, transform .12s ease, background .12s ease, color .12s ease;
  }
  .chip:hover{ filter: brightness(.96); transform: translateY(-1px); }
  .chip.is-active{
    background: var(--chip-active);
    color: #fff;
  }

  /* GRID area */
  .projects-tiles{
    background: var(--cream);
    padding: 1.25rem 0 2.8rem;
  }
  .projects-tiles__inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
  }

  /* ✅ Uniform tiles: vaste hoogte + object-fit cover */
  .tilegrid{
    display:grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: .9rem;
  }

  .tile{
    display:block;
    text-decoration:none;
    color: inherit;
    border: 1px solid rgba(0,0,0,.06);
    background: rgba(0,0,0,.06);
    overflow:hidden;
    position: relative;
  }

  /* vaste media hoogte */
  .tile-media{
    width: 100%;
    height: 220px;          /* ✅ pas aan indien je wil */
    overflow: hidden;
    position: relative;
  }
  .tile-media img{
    width:100%;
    height:100%;
    object-fit: cover;       /* ✅ alles even groot */
    display:block;
    transform: scale(1.001); /* anti hairline gaps */
  }

  /* hover gradient + caption */
  .tile::after{
    content:"";
    position:absolute;
    inset:0;
    background: linear-gradient(0deg, rgba(0,0,0,.50), rgba(0,0,0,0) 60%);
    opacity: 0;
    transition: opacity .15s ease;
    pointer-events:none;
  }
  .tile:hover::after{ opacity: 1; }

  .tile-cap{
    position:absolute;
    left: .8rem;
    right: .8rem;
    bottom: .7rem;
    z-index: 2;
    opacity: 0;
    transform: translateY(6px);
    transition: opacity .15s ease, transform .15s ease;
    color: #fff;
  }
  .tile:hover .tile-cap{
    opacity: 1;
    transform: translateY(0);
  }
  .tile-cap strong{
    display:block;
    font-size: 1.05rem;
    line-height: 1.25;
  }
  .tile-cap span{
    display:block;
    font-size: .92rem;
    opacity: .9;
    margin-top: .2rem;
  }

  .empty{
    padding: 1.2rem;
    border: 1px dashed rgba(0,0,0,.25);
    background: rgba(255,255,255,.55);
    color: var(--muted);
  }

  @media (max-width: 1200px){
    .tilegrid{ grid-template-columns: repeat(3, minmax(0, 1fr)); }
    .tile-media{ height: 210px; }
  }
  @media (max-width: 980px){
    .tilegrid{ grid-template-columns: repeat(2, minmax(0, 1fr)); }
    .tile-media{ height: 200px; }
  }
  @media (max-width: 520px){
    .tilegrid{ grid-template-columns: 1fr; }
    .tile-media{ height: 220px; }
  }
</style>

<div class="projects-page">

  <!-- TOP FILTERS (geen hero/titel) -->
  <section class="projects-top" aria-label="Filters">
    <div class="projects-top__inner">
      <p class="filters-title">Filters</p>

      {% assign items = site.projects | sort: "order" %}
      {% assign alltags = "" | split: "|" %}
      {% for p in items %}
        {% if p.tags %}
          {% for t in p.tags %}
            {% assign alltags = alltags | push: t %}
          {% endfor %}
        {% endif %}
      {% endfor %}
      {% assign alltags = alltags | uniq | sort %}

      <div class="chipbar" id="projFilters">
        <button class="chip is-active" type="button" data-filter="all">All</button>
        {% for t in alltags %}
          <button class="chip" type="button" data-filter="{{ t | downcase | replace: ' ', '-' }}">{{ t }}</button>
        {% endfor %}
      </div>
    </div>
  </section>

  <!-- TILES -->
  <section class="projects-tiles" aria-label="Projecten">
    <div class="projects-tiles__inner">
      {% if items and items.size > 0 %}
        <div class="tilegrid" id="projGrid">
          {% for p in items %}
            {% assign tagstr = "" %}
            {% if p.tags %}
              {% for t in p.tags %}
                {% assign norm = t | downcase | replace: ' ', '-' %}
                {% assign tagstr = tagstr | append: norm | append: " " %}
              {% endfor %}
            {% endif %}

            <a class="tile" href="{{ p.url | relative_url }}" data-tags="{{ tagstr | strip }}">
              <div class="tile-media">
                {% if p.cover %}
                  <img src="{{ p.cover | relative_url }}" alt="{{ p.title }}">
                {% else %}
                  <img src="{{ '/images/projects/placeholder.jpg' | relative_url }}" alt="{{ p.title }}">
                {% endif %}
              </div>

              <div class="tile-cap">
                <strong>{{ p.title }}</strong>
                {% if p.location or p.year %}
                  <span>
                    {% if p.location %}{{ p.location }}{% endif %}
                    {% if p.location and p.year %} · {% endif %}
                    {% if p.year %}{{ p.year }}{% endif %}
                  </span>
                {% endif %}
              </div>
            </a>
          {% endfor %}
        </div>
      {% else %}
        <div class="empty">
          Nog geen projecten gevonden. Voeg projectbestanden toe aan je <code>projects</code>-collectie met <code>cover</code> en <code>tags</code>.
        </div>
      {% endif %}
    </div>
  </section>

</div>

<script>
(function () {
  const filters = document.getElementById('projFilters');
  const grid = document.getElementById('projGrid');
  if (!filters || !grid) return;

  const chips = Array.from(filters.querySelectorAll('.chip'));
  const tiles = Array.from(grid.querySelectorAll('.tile'));

  function setActive(btn){
    chips.forEach(c => c.classList.remove('is-active'));
    btn.classList.add('is-active');
  }

  function apply(filter){
    tiles.forEach(tile => {
      const tags = (tile.getAttribute('data-tags') || '').toLowerCase().trim();
      const tagList = tags ? tags.split(/\s+/) : [];
      const show = (filter === 'all') ? true : tagList.includes(filter);
      tile.style.display = show ? '' : 'none';
    });
  }

  // ✅ robust click handling
  filters.addEventListener('click', function(e){
    const btn = e.target.closest('button.chip');
    if(!btn) return;

    e.preventDefault();
    e.stopPropagation();

    const filter = btn.getAttribute('data-filter') || 'all';
    setActive(btn);
    apply(filter);
  }, true); // capture=true -> beats other handlers

})();
</script>

