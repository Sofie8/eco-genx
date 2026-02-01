---
title: Projecten
layout: default
permalink: /projects/
---

<style>
  /* Hide any default page title injected by theme/layout */
  .page-title,
  .page-header,
  .page-header h1,
  h1.page-title,
  main > h1:first-child{
    display:none !important;
  }

  /* full width page */
  main{ max-width:none !important; padding:0 !important; overflow:visible !important; }
  main > *, main .content, main article, main .page, main .post{
    max-width:none !important; padding:0 !important; margin:0 !important; overflow:visible !important;
  }

  .projects-page{
    --max: 1200px;
    --pad: 1.25rem;
    --cream: var(--eco-cream, #f6f4ee);
    --line: rgba(0,0,0,.10);
    --chip: #d8d8d8;
    --chip-active: #3a3a3a;
  }

  /* TOP FILTERS */
  .projects-top{
    background:#fff;
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

  /* --- CSS-only filter controls (radio + label as chip) --- */
  .projfilter{
    position: absolute;
    left: -9999px;
    width: 1px; height: 1px;
    overflow: hidden;
  }
  .chipbar{
    display:flex;
    flex-wrap:wrap;
    gap: .55rem;
    align-items:center;
  }
  .chip{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    border: 0;
    background: var(--chip);
    color: rgba(0,0,0,.78);
    padding: .5rem .7rem;
    cursor:pointer;
    font: inherit;
    font-size: .95rem;
    line-height: 1.2;
    transition: filter .12s ease, transform .12s ease, background .12s ease, color .12s ease;
    user-select:none;
  }
  .chip:hover{ filter: brightness(.96); transform: translateY(-1px); }

  /* active chip based on checked radio */
  #f-all:checked ~ .projects-top .chip[for="f-all"],
  .projects-page .projfilter:checked + .chip{
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

  /* Uniform tiles */
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

  .tile-media{
    width:100%;
    height: 220px;
    overflow:hidden;
    position: relative;
  }
  .tile-media img{
    width:100%;
    height:100%;
    object-fit: cover;
    display:block;
    transform: scale(1.001);
  }

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
    color: rgba(0,0,0,.62);
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

{% assign items = site.projects | sort: "order" %}

{% comment %}
Collect unique tags + build CSS filter rules.
{% endcomment %}
{% assign alltags = "" | split: "|" %}
{% for p in items %}
  {% if p.tags %}
    {% for t in p.tags %}
      {% assign alltags = alltags | push: t %}
    {% endfor %}
  {% endif %}
{% endfor %}
{% assign alltags = alltags | uniq | sort %}

<style>
  /* CSS-only filtering rules generated from tags */
  {% for t in alltags %}
    {% assign norm = t | downcase | replace: ' ', '-' %}
    #f-{{ norm }}:checked ~ .projects-tiles .tile:not(.tag-{{ norm }}){ display:none !important; }
  {% endfor %}
</style>

<div class="projects-page">

  <!-- radios must be before the sections to use ~ selectors -->
  <input class="projfilter" type="radio" name="pf" id="f-all" checked>

  {% for t in alltags %}
    {% assign norm = t | downcase | replace: ' ', '-' %}
    <input class="projfilter" type="radio" name="pf" id="f-{{ norm }}">
  {% endfor %}

  <section class="projects-top" aria-label="Filters">
    <div class="projects-top__inner">
      <p class="filters-title">Filters</p>

      <div class="chipbar">
        <label class="chip" for="f-all">All</label>
        {% for t in alltags %}
          {% assign norm = t | downcase | replace: ' ', '-' %}
          <label class="chip" for="f-{{ norm }}">{{ t }}</label>
        {% endfor %}
      </div>
    </div>
  </section>

  <section class="projects-tiles" aria-label="Project tiles">
    <div class="projects-tiles__inner">

      {% if items and items.size > 0 %}
        <div class="tilegrid">
          {% for p in items %}
            {%- comment -%}
            Skip if a weird item equals this index page (extra safety)
            {%- endcomment -%}
            {% if p.url == page.url %}{% continue %}{% endif %}

            {% assign klass = "" %}
            {% if p.tags %}
              {% for t in p.tags %}
                {% assign norm = t | downcase | replace: ' ', '-' %}
                {% assign klass = klass | append: " tag-" | append: norm %}
              {% endfor %}
            {% endif %}

            <a class="tile{{ klass }}" href="{{ p.url | relative_url }}">
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
        <div class="empty">Nog geen projecten gevonden.</div>
      {% endif %}

    </div>
  </section>

</div>
