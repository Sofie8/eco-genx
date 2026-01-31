---
title: Over Eco-GenX
layout: default
permalink: /about/
nav:
  order: 2
  tooltip: Over Eco-GenX
about_image_1: /images/about-1.jpg
mission_image_1: /images/about-mission-1.jpg
mission_image_2: /images/about-mission-2.jpg
---

<style>
  /* =======================================================
     About page (tabs like Ossiado + mission/vision like Biologic)
     ======================================================= */

  .about-wrap{
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1.25rem;
    box-sizing: border-box;
  }

  /* ---------- Tabs (no JS) ---------- */
  .tabs { margin: 1.4rem 0 2.2rem; }
  .tabs input { display:none; }

  .tab-labels{
    display:flex;
    gap:.6rem;
    flex-wrap:wrap;
    margin: 0 0 1.1rem;
  }

  .tab-labels label{
    cursor:pointer;
    border:1px solid rgba(0,0,0,.10);
    background: rgba(0,0,0,.02);
    padding: .55rem .95rem;
    border-radius: 999px;
    user-select:none;
  }

  #t1:checked ~ .tab-labels label[for="t1"],
  #t2:checked ~ .tab-labels label[for="t2"],
  #t3:checked ~ .tab-labels label[for="t3"],
  #t4:checked ~ .tab-labels label[for="t4"],
  #t5:checked ~ .tab-labels label[for="t5"]{
    background: rgba(9,45,38,.08);
    border-color: rgba(9,45,38,.16);
  }

  .tab-panel{ display:none; }
  #t1:checked ~ .panels #p1,
  #t2:checked ~ .panels #p2,
  #t3:checked ~ .panels #p3,
  #t4:checked ~ .panels #p4,
  #t5:checked ~ .panels #p5{ display:block; }

  /* ---------- Panel card base ---------- */
  .panel-card{
    border:1px solid rgba(0,0,0,.08);
    background: #fff;
    border-radius: 18px;
    padding: 1.35rem 1.35rem;
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
  }

  .muted{ opacity:.82; }
  .section-title{ margin: 0 0 .6rem; font-size: 1.85rem; line-height:1.15; }
  .lead{ font-size: 1.05rem; line-height: 1.65; max-width: 78ch; }
  .eyebrow{
    font-size: .86rem;
    letter-spacing: .08em;
    text-transform: uppercase;
    opacity: .7;
    margin-bottom: .45rem;
  }

  /* ---------- Who am I layout (Ossiado vibe) ---------- */
  .who-grid{
    display:grid;
    grid-template-columns: 1.05fr 1fr;
    gap: 2rem;
    align-items: start;
  }

  .who-grid img{
    width:100%;
    height: 520px;
    object-fit: cover;
    border-radius: 18px;
    display:block;
    border: 1px solid rgba(0,0,0,.08);
    box-shadow: 0 14px 36px rgba(0,0,0,.10);
  }

  .chips{ display:flex; gap:.5rem; flex-wrap:wrap; margin: 1rem 0 0; }
  .chip{
    border:1px solid rgba(0,0,0,.10);
    background: rgba(9,45,38,.04);
    padding: .35rem .65rem;
    border-radius: 999px;
    font-size: .92rem;
  }

  .btnrow{ display:flex; gap:.8rem; flex-wrap:wrap; margin-top: 1.1rem; }
  .btn{
    display:inline-flex;
    align-items:center;
    gap:.45rem;
    padding:.7rem 1.05rem;
    border-radius: 12px;
    text-decoration:none;
    border:1px solid rgba(0,0,0,.10);
    background: rgba(0,0,0,.02);
    transition: transform .12s ease, box-shadow .12s ease;
  }
  .btn.primary{
    background: rgba(9,45,38,.06);
    border-color: rgba(9,45,38,.14);
  }
  .btn:hover{
    transform: translateY(-1px);
    box-shadow: 0 12px 28px rgba(0,0,0,.08);
  }

  /* ---------- Mission/Vision full-width blocks (Biologic vibe) ---------- */
  /* full-bleed section that breaks out of the theme container */
  .full-bleed{
    width: 100vw;
    margin-left: calc(50% - 50vw);
    margin-right: calc(50% - 50vw);
  }

  .mv-block{
    display:grid;
    grid-template-columns: 1.15fr 1fr;
    min-height: 520px;
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

  /* light panel */
  .mv-text{
    background: #f6f4ee;
    padding: 4.0rem 3.2rem;
    display:flex;
    flex-direction: column;
    justify-content: center;
    border-top: 1px solid rgba(0,0,0,.06);
    border-bottom: 1px solid rgba(0,0,0,.06);
  }

  .mv-text h2{
    margin: 0 0 .8rem;
    font-size: 2.3rem;
    line-height: 1.08;
  }

  .mv-text p{
    margin: 0 0 .9rem;
    font-size: 1.05rem;
    line-height: 1.7;
    max-width: 70ch;
  }

  /* second block swapped (text left, photo right) */
  .mv-block.reverse{
    grid-template-columns: 1fr 1.15fr;
  }

  /* responsive */
  @media (max-width: 980px){
    .who-grid{ grid-template-columns: 1fr; }
    .who-grid img{ height: 360px; }

    .mv-block,
    .mv-block.reverse{
      grid-template-columns: 1fr;
      min-height: auto;
    }
    .mv-text{
      padding: 2.2rem 1.25rem;
    }
    .mv-photo{ height: 360px; }
  }
</style>

<div class="about-wrap">

  <div class="eyebrow">Over Eco-GenX</div>
  <h1 class="section-title">Over Eco-GenX</h1>
  <p class="lead muted">
    Eco-GenX helpt organisaties om milieuvraagstukken aan te pakken met de best beschikbare wetenschap — vertaald naar keuzes en acties die werken in de praktijk.
  </p>

  <div class="tabs">
    <input type="radio" id="t1" name="tabs" checked>
    <input type="radio" id="t2" name="tabs">
    <input type="radio" id="t3" name="tabs">
    <input type="radio" id="t4" name="tabs">
    <input type="radio" id="t5" name="tabs">

    <div class="tab-labels">
      <label for="t1">Wie ben ik?</label>
      <label for="t2">Missie & visie</label>
      <label for="t3">Voor wie</label>
      <label for="t4">Onderzoek</label>
      <label for="t5">Communicatie</label>
    </div>

    <div class="panels">

      <!-- =========================
           TAB 1 — WIE BEN IK
           ========================= -->
      <div class="tab-panel" id="p1">
        <div class="panel-card">
          <div class="who-grid">
            <div>
              <img src="{{ page.about_image_1 | relative_url }}" alt="Sofie Thijs — veldwerk en staalname">
            </div>

            <div>
              <div class="eyebrow">Concept bio</div>
              <h2 style="margin:0 0 .6rem;">Ik ben Sofie Thijs.</h2>

              <p class="muted">
                Als doctor in de biologie en milieu-microbiologie is mijn fascinatie altijd uitgegaan naar de onzichtbare wereld
                van micro-organismen die de gezondheid van onze bodems en landschappen mee bepaalt. Mijn academische reis begon
                aan de Universiteit Hasselt en bracht me via een postdoc in bio-informatica aan de University of Waterloo in Canada
                terug naar waar het allemaal begon: de complexe, levende materie onder onze voeten.
              </p>

              <h3 style="margin:1.1rem 0 .4rem;">Van labo naar landschap</h3>
              <p class="muted">
                Die brug tussen diepgravende wetenschap en concrete milieuproblemen is de rode draad in mijn carrière.
                Mijn focus op praktische oplossingen begon tijdens mijn doctoraat, waarin ik explosieven-etende bacteriën onderzocht
                die de springstof TNT kunnen afbreken — een eerste blik op de immense, onontgonnen kracht van micro-organismen.
              </p>

              <p class="muted">
                Tijdens mijn postdoc werkte ik op het raakvlak van fundamenteel onderzoek en complexe verontreinigingen
                zoals olie, VOCL’s, zware metalen en PFAS. Ik zag ook hoe theoretische kennis vaak moeizaam de weg vindt naar het veld.
                Daarom leg ik me toe op het vertalen van wetenschap naar praktische, uitvoerbare oplossingen.
              </p>

              <p class="muted">
                Om dicht bij de nieuwste doorbraken te blijven, combineer ik Eco-GenX met een deeltijdse aanstelling (20%) als coördinator-navorser
                aan UHasselt (Centrum voor Milieukunde). Zo was ik mede-auteur van de <em>Code van Goede Praktijk Fytoremediatie</em> (OVAM),
                een handleiding om fytoremediatie correct en efficiënt toe te passen in Vlaanderen.
              </p>

              <h3 style="margin:1.1rem 0 .4rem;">Waar staat Eco-GenX voor?</h3>
              <p class="muted">
                <strong>Eco</strong> verwijst naar ecologie: het geheel van natuurlijke processen die we kunnen inzetten voor herstel en veerkracht.
                <strong>GenX</strong> verwijst naar genetica én de “meetbare proof-layer” (DNA/eDNA) waarmee we begrijpen wat er gebeurt,
                kunnen bijsturen, en resultaten kunnen onderbouwen.
              </p>

              <div class="chips">
                <span class="chip">Ecologie</span>
                <span class="chip">Genetica</span>
                <span class="chip">DNA/eDNA</span>
                <span class="chip">Veld ↔ labo ↔ besluitvorming</span>
              </div>

              <div class="btnrow">
                <a class="btn primary" href="{{ '/contact/' | relative_url }}">Contacteer mij</a>
                <a class="btn" href="{{ '/projects/' | relative_url }}">Bekijk projecten</a>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- =========================
           TAB 2 — MISSIE & VISIE
           ========================= -->
      <div class="tab-panel" id="p2">
        <div class="full-bleed">

          <!-- Missie block -->
          <section class="mv-block">
            <div class="mv-photo">
              <img src="{{ page.mission_image_1 | relative_url }}" alt="Eco-GenX missie — natuur-gebaseerde oplossingen">
            </div>
            <div class="mv-text">
              <div class="eyebrow">Missie</div>
              <h2>Data-gedreven, natuur-gebaseerde oplossingen.</h2>
              <p>
                Eco-GenX is dé partner voor data-gedreven, natuur-gebaseerde oplossingen in bodemherstel en landbouw.
                Wij combineren ecologische expertise met genetische precisie om meetbaar bewijs te leveren,
                risico’s te beheren en uw projectdoelen te realiseren.
              </p>
              <p class="muted" style="margin:0;">
                Denk: analyse → ontwerp → monitoring → bijsturing, mét bewijslaag waar klassieke monitoring tekortschiet.
              </p>
            </div>
          </section>

          <!-- Visie block (reversed) -->
          <section class="mv-block reverse">
            <div class="mv-text">
              <div class="eyebrow">Visie</div>
              <h2>De natuur als meest efficiënte technologie.</h2>
              <p>
                Wij werken aan een toekomst waarin de natuur de meest efficiënte technologie is.
                Door biologische processen intelligent te sturen met data, bieden we zekerheid bij complexe milieu- en landbouwprojecten.
                Zo maken we landschappen veerkrachtiger, productiever en schoner.
              </p>
              <p class="muted" style="margin:0;">
                Niet alleen inzetten — maar ook begrijpen, sturen en meten.
              </p>
            </div>
            <div class="mv-photo">
              <img src="{{ page.mission_image_2 | relative_url }}" alt="Eco-GenX visie — veerkrachtige landschappen">
            </div>
          </section>

        </div>
      </div>

      <!-- =========================
           TAB 3 — VOOR WIE
           ========================= -->
      <div class="tab-panel" id="p3">
        <div class="panel-card">
          <h2 style="margin:0 0 .6rem;">Voor wie</h2>
          <p class="muted lead">
            Eco-GenX werkt voor organisaties die natuur-gebaseerde oplossingen willen inzetten én nood hebben aan onderbouwde keuzes,
            monitoring en bewijs.
          </p>
          <ul>
            <li>studie- en adviesbureaus (milieu, bodem, water, ecologie)</li>
            <li>bedrijven met site-, bodem- of waterdossiers</li>
            <li>landbouw- en landschapsprojecten met meet- en stuurbehoefte</li>
            <li>organisaties die bioproducten/bioremediatie in het veld willen verifiëren</li>
          </ul>
          <p class="muted">
            Twijfel je of jouw vraag past? Stuur me je context en ik zeg je snel wat een goede eerste stap is.
          </p>
          <p><a href="{{ '/contact/' | relative_url }}">Contacteer mij →</a></p>
        </div>
      </div>

      <!-- =========================
           TAB 4 — ONDERZOEK
           ========================= -->
      <div class="tab-panel" id="p4">
        <div class="panel-card">
          <h2 style="margin:0 0 .6rem;">Onderzoek</h2>
          <p class="muted lead">
            (Hier komt jouw onderzoekslijn / expertise. Ik heb dit alvast als structuur gezet — jij kan later aanvullen.)
          </p>
          <ul>
            <li><strong>Microbiële processen:</strong> eDNA, functionele genen, community shifts, “wat werkt waarom?”</li>
            <li><strong>Complexe verontreinigingen:</strong> olie, VOCL’s, zware metalen, PFAS</li>
            <li><strong>Fytotechnologie:</strong> ontwerp, monitoring, evaluatie en opschaling</li>
            <li><strong>Bio-informatica:</strong> interpretatie van DNA-data naar besluitvorming</li>
          </ul>
        </div>
      </div>

      <!-- =========================
           TAB 5 — COMMUNICATIE
           ========================= -->
      <div class="tab-panel" id="p5">
        <div class="panel-card">
          <h2 style="margin:0 0 .6rem;">Communicatie</h2>
          <p class="muted lead">
            (Hier zet je artikels, lezingen, workshops en media. Handig is om dit later te koppelen aan een lijst.)
          </p>
          <ul>
            <li><strong>Code van Goede Praktijk Fytoremediatie</strong> (OVAM) — mede-auteur</li>
            <li><strong>Lezing</strong> — titel / event / jaar</li>
            <li><strong>Artikel</strong> — titel / link</li>
          </ul>
        </div>
      </div>

    </div>
  </div>

</div>
