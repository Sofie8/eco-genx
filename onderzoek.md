---
title: Onderzoek & ontwikkeling
layout: default
permalink: over/onderzoek/

# ✅ logo’s (upload zelf naar /images/logos/)
logos:
  - src: /images/logos/vmm.svg
    alt: Vlaamse Milieumaatschappij
    href: https://www.vmm.be/
  - src: /images/logos/uhasselt.svg
    alt: UHasselt
    href: https://www.uhasselt.be/
  - src: /images/logos/iflux.svg
    alt: iFLUX
    href: https://iflux.be/

# ✅ Lopende projecten via Eco-GenX (vennootschap)
ongoing_company:
  - title: "Barebeek (Zemst) — PFAS piloot & demonstratie"
    subtitle: "Nature-based ingrepen om PFAS-vang efficiënter te maken in de sedimentvang, met multi-line-of-evidence monitoring."
    body: >
      Pilootproject rond innovatieve in-situ sanering om verspreiding van PFAS via sediment en oppervlaktewater te reduceren.
      Traject met nulmeting → ontwerp → real-scale implementatie → effectmonitoring, inclusief concentraties én fluxen (richting grondwater/oppervlaktewater).
    tags: ["Eco-GenX", "PFAS", "wetlands", "monitoring"]
  - title: "PFAS RESOLVE — evidence & monitoring (voorbeeld)"
    subtitle: "Korte uitleg wat jij wil tonen (later aanvullen)."
    body: "Vul hier later details aan: doel, aanpak, deliverables, partners, status."
    tags: ["Eco-GenX", "PFAS", "evidence"]

# ✅ Lopende academische projecten (UHasselt 20%)
ongoing_academic:
  - title: "Academisch project — (placeholder)"
    subtitle: "1 zin: focus, consortium, jouw rol."
    body: "Vul aan met doel, methodes, en wat het oplevert."
    tags: ["UHasselt", "onderzoek", "monitoring"]

# ✅ Archief 2019–2024 (1 rubriek)
archive_2019_2024:
  - title: "Titel archiefproject — korte omschrijving"
    subtitle: "1 zin: waarom relevant, wat werd gedaan."
    body: "Hier kan je later 3–6 regels context + jouw rol + outcome toevoegen."
    tags: ["Eco-GenX", "bodem"]
---

<style>
  /* =========================================================
     ONDERZOEK — hero + accordions (ISOdetect/HPC-style)
     Scope: .rnd
     ========================================================= */

  /* full width (zoals je services/projects) */
  main{ max-width:none !important; padding:0 !important; overflow:visible !important; }
  main > *, main .content, main article, main .page, main .post{
    max-width:none !important; padding:0 !important; margin:0 !important; overflow:visible !important;
  }

  .rnd{
    --max: 1200px;
    --pad: 1.25rem;
    --cream: var(--eco-cream, #f6f4ee);
    --green: var(--eco-dark, #0b3b2f);
    --green2: var(--eco-dark-2, #082a22);
    --ink: rgba(0,0,0,.86);
    --muted: rgba(0,0,0,.66);
    --line: rgba(0,0,0,.10);
  }

  /* HERO */
  .rnd-hero{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    min-height: 520px;
    background-image: url("{{ '/images/onderzoek-hero.jpg' | relative_url }}");
    background-size: cover;
    background-position: center;
  }
  .rnd-hero::before{
    content:"";
    position:absolute; inset:0;
    background: linear-gradient(90deg,
      rgba(8,42,34,.86) 0%,
      rgba(8,42,34,.64) 46%,
      rgba(8,42,34,.22) 100%);
  }

  .rnd-hero__inner{
    position: relative;
    max-width: var(--max);
    margin: 0 auto;
    padding: 4.2rem var(--pad) 3.1rem;
    display:grid;
    grid-template-columns: 1.15fr .85fr;
    gap: 2rem;
    align-items: center;
    color: rgba(255,255,255,.92);
  }

  .rnd-eyebrow{
    font-size: .86rem;
    letter-spacing: .10em;
    text-transform: uppercase;
    opacity: .85;
    margin-bottom: .65rem;
  }
  .rnd-hero h1{
    margin:0 0 .75rem;
    font-size: 3.05rem;
    line-height: 1.04;
    letter-spacing: .02em;
    max-width: 22ch;
  }
  .rnd-hero p{
    margin:0;
    opacity: .92;
    line-height: 1.75;
    max-width: 80ch;
    font-size: 1.05rem;
  }

  .rnd-panel{
    border: 1px solid rgba(255,255,255,.16);
    border-radius: 18px;
    padding: 1.05rem 1.1rem;
    background: rgba(255,255,255,.06);
    box-shadow: 0 18px 44px rgba(0,0,0,.18);
  }
  .rnd-panel h3{
    margin:0 0 .55rem;
    font-size: 1.05rem;
    letter-spacing: .06em;
    text-transform: uppercase;
    opacity: .95;
  }
  .rnd-panel ul{
    margin:.35rem 0 0;
    padding-left: 1.1rem;
    opacity: .92;
    line-height: 1.65;
  }
  .rnd-panel li{ margin:.35rem 0; }

  /* logo row */
  .logo-row{
    margin-top: 1rem;
    display:flex;
    flex-wrap: wrap;
    gap: .65rem .95rem;
    align-items: center;
  }
  .logo-row a{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    padding:.35rem .55rem;
    border-radius: 12px;
    border: 1px solid rgba(255,255,255,.14);
    background: rgba(255,255,255,.06);
    text-decoration:none;
  }
  .logo-row img{
    height: 28px;
    width: auto;
    display:block;
    filter: brightness(1.02);
    opacity: .95;
  }

  /* BODY */
  .rnd-body{
    background: var(--cream);
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;
    padding: 2.6rem 0 3.2rem;
    border-top: 1px solid rgba(0,0,0,.06);
  }
  .rnd-body__inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
  }

  .section{
    margin-top: 2.25rem;
  }
  .section h2{
    margin:0 0 .6rem;
    font-size: 2.05rem;
    line-height: 1.12;
    color: var(--ink);
  }
  .section .lead{
    margin:0 0 1.2rem;
    color: var(--muted);
    max-width: 85ch;
    line-height: 1.75;
  }

  /* ACCORDION card */
  .acc{
    border-radius: 22px;
    overflow: hidden;
    border: 1px solid rgba(0,0,0,.10);
    background: rgba(255,255,255,.55);
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
    margin-bottom: 1.05rem;
  }

  details.acc > summary{
    list-style: none;
    cursor: pointer;
    padding: 1.05rem 1.1rem;
    display:flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 1rem;
    background: rgba(0,0,0,.06);
  }
  details.acc > summary::-webkit-details-marker{ display:none; }

  .acc-title{
    font-weight: 650;
    color: rgba(0,0,0,.86);
    line-height: 1.35;
    font-size: 1.1rem;
    margin: 0;
  }
  .acc-sub{
    margin:.25rem 0 0;
    color: rgba(0,0,0,.62);
    line-height: 1.6;
    max-width: 85ch;
  }

  /* plus button */
  .acc-toggle{
    flex: 0 0 auto;
    width: 34px;
    height: 34px;
    border-radius: 999px;
    border: 1px solid rgba(0,0,0,.18);
    background: rgba(255,255,255,.65);
    position: relative;
    margin-top: .05rem;
  }
  .acc-toggle::before,
  .acc-toggle::after{
    content:"";
    position:absolute;
    left:50%; top:50%;
    width: 14px; height: 2px;
    background: rgba(0,0,0,.65);
    transform: translate(-50%,-50%);
  }
  .acc-toggle::after{
    transform: translate(-50%,-50%) rotate(90deg);
    transition: transform .14s ease;
  }
  details[open] .acc-toggle::after{
    transform: translate(-50%,-50%) rotate(0deg);
  }

  .acc-body{
    padding: 1.05rem 1.1rem 1.15rem;
    color: rgba(0,0,0,.74);
    line-height: 1.75;
  }

  .tagrow{
    display:flex;
    flex-wrap: wrap;
    gap: .45rem;
    margin-top: .75rem;
  }
  .tag{
    font-size: .82rem;
    padding: .28rem .6rem;
    border-radius: 999px;
    border: 1px solid rgba(11,59,47,.22);
    background: rgba(11,59,47,.06);
    color: rgba(11,59,47,.92);
  }

  .divider{
    margin: 2.25rem 0 0;
    border: 0;
    border-top: 1px solid rgba(0,0,0,.10);
  }

  @media (max-width: 980px){
    .rnd-hero__inner{ grid-template-columns: 1fr; padding: 3.2rem var(--pad) 2.6rem; }
    .rnd-hero h1{ font-size: 2.25rem; }
    .logo-row img{ height: 26px; }
  }
</style>

<div class="rnd">

  <!-- HERO -->
  <section class="rnd-hero" aria-label="Onderzoek hero">
    <div class="rnd-hero__inner">
      <div>
        <div class="rnd-eyebrow">Eco-GenX · onderzoek & ontwikkeling</div>
        <h1>Van wetenschap naar terrein</h1>
        <p>
          Ik ontwikkel en test meetbare innovaties rond bodem-, water- en PFAS-herstel:
          nature-based ontwerpen, evidence-plannen en monitoring die <em>decision-ready</em> antwoorden opleveren.
        </p>

        {% if page.logos %}
          <div class="logo-row" aria-label="Partners & context">
            {% for l in page.logos %}
              {% if l.href %}
                <a href="{{ l.href }}" target="_blank" rel="noopener">
                  <img src="{{ l.src | relative_url }}" alt="{{ l.alt }}">
                </a>
              {% else %}
                <a href="#" onclick="return false;">
                  <img src="{{ l.src | relative_url }}" alt="{{ l.alt }}">
                </a>
              {% endif %}
            {% endfor %}
          </div>
        {% endif %}
      </div>

      <div class="rnd-panel">
        <h3>Hoe ik dit toon</h3>
        <ul>
          <li>lopende projecten (Eco-GenX)</li>
          <li>academische projecten (UHasselt, 20%)</li>
          <li>archief 2019–2024</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- BODY -->
  <section class="rnd-body">
    <div class="rnd-body__inner">

      <!-- Eco-GenX -->
      <div class="section">
        <h2>Lopende projecten — Eco-GenX</h2>
        <p class="lead">
          Projecten waarbij ik betrokken ben via Eco-GenX / vennootschap (advies, ontwerp, monitoring, proof-of-impact).
        </p>

        {% for p in page.ongoing_company %}
          <details class="acc">
            <summary>
              <div>
                <div class="acc-title">{{ p.title }}</div>
                {% if p.subtitle %}<div class="acc-sub">{{ p.subtitle }}</div>{% endif %}
              </div>
              <div class="acc-toggle" aria-hidden="true"></div>
            </summary>
            <div class="acc-body">
              {{ p.body }}
              {% if p.tags %}
                <div class="tagrow">
                  {% for t in p.tags %}
                    <span class="tag">{{ t }}</span>
                  {% endfor %}
                </div>
              {% endif %}
            </div>
          </details>
        {% endfor %}
      </div>

      <hr class="divider">

      <!-- Academisch -->
      <div class="section">
        <h2>Lopende academische projecten — UHasselt (20%)</h2>
        <p class="lead">
          Projecten vanuit mijn academische aanstelling. Zo blijft het onderscheid helder voor de lezer.
        </p>

        {% for p in page.ongoing_academic %}
          <details class="acc">
            <summary>
              <div>
                <div class="acc-title">{{ p.title }}</div>
                {% if p.subtitle %}<div class="acc-sub">{{ p.subtitle }}</div>{% endif %}
              </div>
              <div class="acc-toggle" aria-hidden="true"></div>
            </summary>
            <div class="acc-body">
              {{ p.body }}
              {% if p.tags %}
                <div class="tagrow">
                  {% for t in p.tags %}
                    <span class="tag">{{ t }}</span>
                  {% endfor %}
                </div>
              {% endif %}
            </div>
          </details>
        {% endfor %}
      </div>

      <hr class="divider">

      <!-- Archief -->
      <div class="section">
        <h2>Archief — 2019–2024</h2>
        <p class="lead">
          Afgeronde of oudere trajecten samengevoegd in één rubriek. Gebruik tags om “Eco-GenX” versus “UHasselt” duidelijk te houden.
        </p>

        {% for p in page.archive_2019_2024 %}
          <details class="acc">
            <summary>
              <div>
                <div class="acc-title">{{ p.title }}</div>
                {% if p.subtitle %}<div class="acc-sub">{{ p.subtitle }}</div>{% endif %}
              </div>
              <div class="acc-toggle" aria-hidden="true"></div>
            </summary>
            <div class="acc-body">
              {{ p.body }}
              {% if p.tags %}
                <div class="tagrow">
                  {% for t in p.tags %}
                    <span class="tag">{{ t }}</span>
                  {% endfor %}
                </div>
              {% endif %}
            </div>
          </details>
        {% endfor %}
      </div>

    </div>
  </section>

</div>
