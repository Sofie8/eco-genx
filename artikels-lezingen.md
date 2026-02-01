---
title: Artikels & lezingen
layout: default
permalink: /over/artikels-lezingen/
nav:
  order: 3
  tooltip: Artikels & lezingen

# ======= CONTENT DATA (pas dit aan) =======
hero_image: /images/over/artikels-hero.jpg

# Optioneel: je "Code van goede praktijk"
code:
  title: "Code van goede praktijk (OVAM)"
  subtitle: "Praktische richtlijnen voor burgers en terreinbeheer — helder, toepasbaar en onderbouwd."
  image: /images/over/code-goede-praktijk.jpg
  pdf: /files/code-goede-praktijk.pdf   # optioneel (zet leeg als je geen PDF wil)
  bullets:
    - "Voor wie: burgers, lokale besturen, terreinbeheerders"
    - "Focus: heldere stappen, risico-inschatting, praktische maatregelen"
    - "Gebruik: als leidraad in communicatie & praktijktoepassing"

# Artikels (kaartjes)
articles:
  - title: "Artikel titel 1"
    where: "Platform / krant / blog"
    year: "2026"
    link: ""  # bv. https://...
    note: "1 zin context over onderwerp, doelgroep of impact."
  - title: "Artikel titel 2"
    where: "Platform / organisatie"
    year: "2025"
    link: ""
    note: "Korte beschrijving."

# Lezingen (kaartjes)
talks:
  - title: "Lezing voor burgers (voorbeeld)"
    where: "Gemeente / zaal / event"
    year: "2026"
    note: "Interactieve sessie: uitleg, Q&A, praktische tips."
  - title: "Infosessie voor buurtcomité (voorbeeld)"
    where: "Buurt / wijk"
    year: "2025"
    note: "Toegepast: meetplan, interpretatie, wat wel/niet werkt."

# Foto’s van lezingen (gallery)
# Je kan zoveel items toevoegen als je wil
lecture_photos:
  - src: /images/over/lezingen/lezing-01.jpg
    caption: "Lezing / infosessie (caption optioneel)"
  - src: /images/over/lezingen/lezing-02.jpg
    caption: "Q&A met burgers (caption optioneel)"
---

<style>
  /* =========================================================
     Artikels & lezingen — full-bleed hero + blocks
     Scoped to .al-page
     ========================================================= */

  /* full width page */
  main{ max-width:none !important; padding:0 !important; overflow:visible !important; }
  main > *, main .content, main article, main .page, main .post{
    max-width:none !important; padding:0 !important; margin:0 !important; overflow:visible !important;
  }

  .al-page{
    --max: 1200px;
    --pad: 1.25rem;

    --cream: var(--eco-cream, #f6f4ee);
    --green: var(--eco-dark, #0b3b2f);
    --green2: var(--eco-dark-2, #082a22);

    --ink: rgba(0,0,0,.86);
    --muted: rgba(0,0,0,.66);
    --line: rgba(0,0,0,.10);

    --card: rgba(255,255,255,.65);
  }

  /* HERO */
  .al-hero{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    min-height: 520px;
    background: #082a22;
    overflow: hidden;
  }
  .al-hero img{
    position:absolute; inset:0;
    width:100%; height:100%;
    object-fit: cover;
    display:block;
  }
  .al-hero::before{
    content:"";
    position:absolute; inset:0;
    background: linear-gradient(90deg,
      rgba(8,42,34,.86) 0%,
      rgba(8,42,34,.62) 45%,
      rgba(8,42,34,.18) 100%);
  }
  .al-hero__inner{
    position: relative;
    min-height: 520px;
    display:flex;
    align-items:flex-end;
    padding: 3.1rem 0 2.6rem;
  }
  .al-hero__inner .wrap{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
    color: rgba(255,255,255,.92);
  }
  .al-eyebrow{
    font-size:.86rem;
    letter-spacing:.10em;
    text-transform: uppercase;
    opacity:.88;
    margin: 0 0 .7rem;
  }
  .al-title{
    margin:0 0 .6rem;
    font-size: 3rem;
    line-height:1.04;
    letter-spacing:.02em;
    max-width: 22ch;
  }
  .al-lead{
    margin:0;
    max-width: 80ch;
    line-height:1.7;
    font-size: 1.08rem;
    opacity:.92;
  }

  /* SECTION WRAPPER */
  .al-section{
    background: var(--cream);
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;
    padding: 2.6rem 0;
    border-top: 1px solid rgba(0,0,0,.06);
  }
  .al-section .wrap{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
  }

  .al-h2{
    margin:0 0 .55rem;
    font-size: 1.8rem;
    color: var(--ink);
    line-height:1.15;
  }
  .al-intro{
    margin:0 0 1.2rem;
    color: var(--muted);
    max-width: 85ch;
    line-height:1.7;
  }

  /* Cards */
  .grid{
    display:grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 1.1rem;
  }
  .card{
    background: var(--card);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    overflow:hidden;
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
    padding: 1.1rem 1.15rem;
  }
  .card h3{
    margin:0 0 .4rem;
    font-size: 1.1rem;
    line-height:1.25;
    color: var(--ink);
  }
  .meta{
    color: var(--muted);
    font-size: .95rem;
    display:flex;
    flex-wrap:wrap;
    gap:.5rem;
    margin-bottom:.55rem;
  }
  .card p{
    margin:0;
    color: rgba(0,0,0,.74);
    line-height:1.65;
  }
  .card a{
    display:inline-block;
    margin-top:.75rem;
    text-decoration:none;
    color: rgba(11,59,47,.92);
    font-weight: 650;
    border-bottom: 1px solid rgba(11,59,47,.35);
    padding-bottom:.06rem;
  }

  /* CODE BLOCK (image + text) */
  .code-block{
    display:grid;
    grid-template-columns: 1.05fr .95fr;
    gap: 1.3rem;
    align-items: stretch;
  }
  .code-media{
    border-radius: 18px;
    overflow:hidden;
    border: 1px solid rgba(0,0,0,.10);
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
    background: rgba(255,255,255,.55);
  }
  .code-media img{
    width:100%;
    height:100%;
    min-height: 360px;
    object-fit: cover;
    display:block;
  }
  .code-text{
    background: rgba(255,255,255,.55);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    padding: 1.4rem 1.5rem;
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
    display:flex;
    flex-direction:column;
    justify-content:center;
  }
  .code-text h3{
    margin:0 0 .35rem;
    font-size: 1.25rem;
    color: var(--ink);
  }
  .code-text .sub{
    margin:0 0 .9rem;
    color: var(--muted);
    line-height:1.65;
  }
  .code-text ul{
    margin: 0;
    padding-left: 1.1rem;
    color: rgba(0,0,0,.74);
    line-height:1.7;
  }
  .code-actions{
    margin-top: 1rem;
    display:flex;
    gap:.7rem;
    flex-wrap:wrap;
  }
  .btn{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    padding: .65rem .9rem;
    border-radius: 12px;
    border: 1px solid rgba(11,59,47,.22);
    background: rgba(11,59,47,.06);
    text-decoration:none;
    color: rgba(11,59,47,.92);
    font-weight: 650;
    white-space:nowrap;
  }
  .btn:hover{ background: rgba(11,59,47,.10); }

  /* GALLERY */
  .gal{
    display:grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 1rem;
    margin-top: 1.1rem;
  }
  .gal figure{
    margin:0;
    border-radius: 18px;
    overflow:hidden;
    border: 1px solid rgba(0,0,0,.08);
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
    background: rgba(255,255,255,.55);
  }
  .gal img{
    width:100%;
    height: 260px;
    object-fit: cover;
    display:block;
  }
  .cap{
    padding: .75rem .85rem;
    color: rgba(0,0,0,.72);
    font-size: .95rem;
    line-height: 1.5;
  }

  @media (max-width: 980px){
    .al-title{ font-size: 2.2rem; }
    .al-hero, .al-hero__inner{ min-height: 520px; }
    .grid{ grid-template-columns: 1fr; }
    .code-block{ grid-template-columns: 1fr; }
    .code-media img{ min-height: 320px; }
    .gal{ grid-template-columns: 1fr; }
    .gal img{ height: 320px; }
  }
</style>

<div class="al-page">

  <!-- HERO -->
  <header class="al-hero">
    {% if page.hero_image %}
      <img src="{{ page.hero_image | relative_url }}" alt="Artikels & lezingen">
    {% endif %}
    <div class="al-hero__inner">
      <div class="wrap">
        <div class="al-eyebrow">Eco-GenX · Over</div>
        <h1 class="al-title">Artikels & lezingen</h1>
        <p class="al-lead">
          Praktijkgerichte communicatie — van heldere richtlijnen en artikels tot lezingen voor burgers,
          lokale besturen en stakeholders. Altijd met focus op meetbaarheid en toepasbaarheid.
        </p>
      </div>
    </div>
  </header>

  <!-- CODE VAN GOEDE PRAKTIJK -->
  <section class="al-section" aria-label="Code van goede praktijk">
    <div class="wrap">
      <h2 class="al-h2">{{ page.code.title }}</h2>
      <p class="al-intro">{{ page.code.subtitle }}</p>

      <div class="code-block">
        <div class="code-media">
          {% if page.code.image %}
            <img src="{{ page.code.image | relative_url }}" alt="Code van goede praktijk">
          {% endif %}
        </div>

        <div class="code-text">
          <h3>Wat je mag verwachten</h3>
          {% if page.code.bullets %}
            <ul>
              {% for b in page.code.bullets %}
                <li>{{ b }}</li>
              {% endfor %}
            </ul>
          {% endif %}

          <div class="code-actions">
            {% if page.code.pdf and page.code.pdf != "" %}
              <a class="btn" href="{{ page.code.pdf | relative_url }}">Download PDF →</a>
            {% endif %}
            <a class="btn" href="{{ '/contact/' | relative_url }}">Vraag samenwerking →</a>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ARTIKELS -->
  <section class="al-section" aria-label="Artikels">
    <div class="wrap">
      <h2 class="al-h2">Artikels</h2>
      <p class="al-intro">Selectie van publicaties en bijdragen. (Vul aan of link door naar externe pagina’s.)</p>

      {% if page.articles and page.articles.size > 0 %}
        <div class="grid">
          {% for a in page.articles %}
            <div class="card">
              <h3>{{ a.title }}</h3>
              <div class="meta">
                {% if a.where %}<span>{{ a.where }}</span>{% endif %}
                {% if a.year %}<span>· {{ a.year }}</span>{% endif %}
              </div>
              {% if a.note %}<p>{{ a.note }}</p>{% endif %}
              {% if a.link and a.link != "" %}
                <a href="{{ a.link }}" target="_blank" rel="noopener">Lees artikel →</a>
              {% endif %}
            </div>
          {% endfor %}
        </div>
      {% else %}
        <div class="card">
          <h3>Nog geen artikels ingevuld</h3>
          <p>Vul de lijst aan in de front matter onder <code>articles:</code>.</p>
        </div>
      {% endif %}
    </div>
  </section>

  <!-- LEZINGEN -->
  <section class="al-section" aria-label="Lezingen">
    <div class="wrap">
      <h2 class="al-h2">Lezingen</h2>
      <p class="al-intro">Voor burgers, lokale besturen en organisaties — met ruimte voor vragen en praktische vertaling.</p>

      {% if page.talks and page.talks.size > 0 %}
        <div class="grid">
          {% for t in page.talks %}
            <div class="card">
              <h3>{{ t.title }}</h3>
              <div class="meta">
                {% if t.where %}<span>{{ t.where }}</span>{% endif %}
                {% if t.year %}<span>· {{ t.year }}</span>{% endif %}
              </div>
              {% if t.note %}<p>{{ t.note }}</p>{% endif %}
              <a href="{{ '/contact/' | relative_url }}">Boek een lezing →</a>
            </div>
          {% endfor %}
        </div>
      {% endif %}

      {% if page.lecture_photos and page.lecture_photos.size > 0 %}
        <h2 class="al-h2" style="margin-top:2.2rem;">Beelden</h2>
        <div class="gal">
          {% for g in page.lecture_photos %}
            <figure>
              <img src="{{ g.src | relative_url }}" alt="{{ g.caption | default: 'Lezing' }}">
              {% if g.caption %}<figcaption class="cap">{{ g.caption }}</figcaption>{% endif %}
            </figure>
          {% endfor %}
        </div>
      {% endif %}
    </div>
  </section>

</div>
