---
title: Over Eco-GenX
layout: default
permalink: /about/
nav:
  order: 2
  tooltip: Over Eco-GenX
about_image_1: /images/about-1.jpg
about_image_2: /images/about-2.jpg
---

<style>
  /* ---------- About hero (Ossiado-ish: photo + text) ---------- */
  .about-wrap{
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1.25rem;
    box-sizing: border-box;
  }

  .about-hero{
    display:grid;
    grid-template-columns: 1.05fr 1fr;
    gap: 2.1rem;
    align-items:center;
    margin: 1.2rem 0 2.2rem;
  }

  .about-hero img{
    width:100%;
    height: 460px;
    object-fit: cover;
    border-radius: 18px;
    display:block;
    box-shadow: 0 14px 36px rgba(0,0,0,.10);
    border: 1px solid rgba(0,0,0,.08);
  }

  .eyebrow{
    font-size: .86rem;
    letter-spacing: .08em;
    text-transform: uppercase;
    opacity: .75;
    margin-bottom: .45rem;
  }

  .about-hero h1{ margin:0 0 .55rem; font-size: 2.25rem; line-height: 1.1; }
  .lead{
    font-size: 1.08rem;
    line-height: 1.65;
    max-width: 72ch;
    opacity: .92;
  }

  .chips{ display:flex; gap:.5rem; flex-wrap:wrap; margin: 1.05rem 0 0; }
  .chip{
    border:1px solid rgba(0,0,0,.10);
    background: rgba(9,45,38,.04);
    padding: .35rem .65rem;
    border-radius: 999px;
    font-size: .92rem;
  }

  .btnrow{ display:flex; gap:.8rem; flex-wrap:wrap; margin-top:1.1rem; }
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

  /* ---------- Sections ---------- */
  .section{
    margin: 2.8rem 0;
    padding-top: 1.3rem;
    border-top: 1px solid rgba(0,0,0,.08);
  }
  .section h2{ margin: 0 0 .6rem; font-size: 1.7rem; }
  .muted{ opacity: .82; }
  .section-intro{ max-width: 78ch; }

  /* ---------- Tabs (no JS) ---------- */
  .tabs { margin-top: 1.2rem; }
  .tabs input { display:none; }

  .tab-labels{
    display:flex;
    gap:.6rem;
    flex-wrap:wrap;
    margin: 0 0 1rem;
  }

  .tab-labels label{
    cursor:pointer;
    border:1px solid rgba(0,0,0,.10);
    background: rgba(0,0,0,.02);
    padding: .5rem .85rem;
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

  .tab-panel{
    display:none;
    border:1px solid rgba(0,0,0,.08);
    background: #fff;
    border-radius: 18px;
    padding: 1.25rem 1.25rem;
    box-shadow: 0 14px 36px rgba(0,0,0,.06);
  }

  #t1:checked ~ .panels #p1,
  #t2:checked ~ .panels #p2,
  #t3:checked ~ .panels #p3,
  #t4:checked ~ .panels #p4,
  #t5:checked ~ .panels #p5{
    display:block;
  }

  /* ---------- Two-col photo + text ---------- */
  .two-col{
    display:grid;
    grid-template-columns: 1fr 1fr;
    gap: 1.6rem;
    align-items:start;
    margin-top: 1.4rem;
  }

  .two-col img{
    width:100%;
    height: 360px;
    object-fit: cover;
    border-radius: 18px;
    display:block;
    border: 1px solid rgba(0,0,0,.08);
    box-shadow: 0 14px 36px rgba(0,0,0,.08);
  }

  @media (max-width: 980px){
    .about-hero{ grid-template-columns: 1fr; }
    .about-hero img{ height: 340px; }
    .two-col{ grid-template-columns: 1fr; }
    .two-col img{ height: 300px; }
  }
</style>

<div class="about-wrap">

  <!-- HERO: photo + intro -->
  <section class="about-hero">
    <div>
      <img src="{{ page.about_image_1 | relative_url }}" alt="Sofie Thijs — veldwerk en staalname">
    </div>

    <div>
      <div class="eyebrow">Wie ben ik?</div>
      <h1>Ik ben Sofie Thijs.</h1>

      <p class="lead">
        Als doctor in de biologie en milieu-microbiologie ben ik gefascineerd door de onzichtbare wereld van micro-organismen
        die mee bepaalt hoe gezond onze bodems en landschappen zijn.
        Mijn traject begon aan de Universiteit Hasselt en bracht me via een postdoc bio-informatica aan de University of Waterloo (Canada)
        terug naar waar het voor mij altijd om draaide: de complexe, levende materie onder onze voeten.
      </p>

      <div class="chips">
        <span class="chip">Restore</span>
        <span class="chip">MicroProof</span>
        <span class="chip">PlantIQ</span>
        <span class="chip">DNA/eDNA & PCR</span>
        <span class="chip">Veld ↔ labo ↔ besluitvorming</span>
      </div>

      <div class="btnrow">
        <a class="btn primary" href="{{ '/contact/' | relative_url }}">Contacteer mij</a>
        <a class="btn" href="{{ '/projects/' | relative_url }}">Bekijk projecten</a>
      </div>
    </div>
  </section>

  <!-- Narrative section -->
  <section class="section">
    <h2>Van labo naar landschap</h2>
    <p class="section-intro muted">
      De rode draad in mijn carrière is de brug tussen diepgravende wetenschap en concrete milieuproblemen.
      Mijn focus op praktische oplossingen begon al tijdens mijn doctoraat, waarin ik de unieke eigenschappen onderzocht van bacteriën
      die de springstof TNT kunnen afbreken. Dat liet me vroeg zien hoeveel onontgonnen kracht er zit in micro-organismen.
    </p>

    <p class="section-intro muted">
      Tijdens mijn postdoc werkte ik verder op het raakvlak van fundamenteel onderzoek en complexe verontreinigingen
      (o.a. olie, VOCL’s, zware metalen en PFAS). Tegelijk zag ik van dichtbij hoe theoretische kennis vaak moeizaam haar weg naar het veld vindt.
      Daarom heb ik me toegelegd op het vertalen van wetenschap naar praktische, uitvoerbare oplossingen.
    </p>

    <p class="section-intro muted">
      Om dicht bij de nieuwste wetenschappelijke doorbraken te blijven, combineer ik Eco-GenX met een deeltijdse aanstelling (20%)
      als coördinator-navorser aan UHasselt (Centrum voor Milieukunde).
      Zo was ik mede-auteur van de <em>Code van Goede Praktijk Fytoremediatie</em> (in opdracht van OVAM),
      een handleiding om fytoremediatie correct en efficiënt toe te passen in Vlaanderen.
    </p>
  </section>

  <!-- Tabs block -->
  <section class="section">
    <h2>Missie, ambitie en visie</h2>
    <p class="section-intro muted">
      Ik geloof dat natuur-gebaseerde oplossingen pas echt schaalbaar worden als we ze niet alleen inzetten, maar ook
      <strong>begrijpen, sturen en meten</strong>.
    </p>

    <div class="tabs">
      <input type="radio" id="t1" name="tabs" checked>
      <input type="radio" id="t2" name="tabs">
      <input type="radio" id="t3" name="tabs">
      <input type="radio" id="t4" name="tabs">
      <input type="radio" id="t5" name="tabs">

      <div class="tab-labels">
        <label for="t1">Missie</label>
        <label for="t2">Ambitie</label>
        <label for="t3">Visie</label>
        <label for="t4">Voor wie</label>
        <label for="t5">Artikels & lezingen</label>
      </div>

      <div class="panels">
        <div class="tab-panel" id="p1">
          <h3>Missie</h3>
          <p class="muted">
            Eco-GenX helpt organisaties om milieuvraagstukken aan te pakken met de best beschikbare wetenschap — vertaald naar
            keuzes en acties die werken in de praktijk. Niet met beloftes, maar met <strong>decision-ready resultaten</strong>.
          </p>
        </div>

        <div class="tab-panel" id="p2">
          <h3>Ambitie</h3>
          <p class="muted">
            Ik wil een herkenbare partner zijn voor projecten die natuur-gedreven oplossingen inzetten,
            maar tegelijk nood hebben aan <strong>bewijs, monitoring en onderbouwde besluitvorming</strong>.
          </p>
          <ul>
            <li>trajecten uitwerken van analyse → ontwerp → monitoring → bijsturing</li>
            <li>DNA/eDNA inzetten als “proof layer” waar klassieke monitoring tekortschiet</li>
            <li>een brug slaan tussen veld, labo en strategie</li>
          </ul>
        </div>

        <div class="tab-panel" id="p3">
          <h3>Visie</h3>
          <p class="muted">
            Klassieke én bio-gebaseerde saneringen pakken vaak de symptomen aan, terwijl de onderliggende processen een “zwarte doos” blijven.
            Ik ben ervan overtuigd dat we moeten evolueren naar systemen waarbij we natuurlijke processen niet alleen activeren, maar ook
            <strong>meetbaar maken</strong> en <strong>gericht kunnen sturen</strong>.
          </p>

          <p class="muted">
            Dat rust op drie pijlers:
          </p>

          <ul>
            <li>
              <strong>De microbiële motor (MicroProof):</strong> via DNA-technieken (eDNA) openen we de zwarte doos:
              welke microben zijn actief, welke functionele genen spelen mee, en waarom werkt iets wél of niet?
            </li>
            <li>
              <strong>De juiste plant (PlantIQ):</strong> microben doen het niet alleen. Succes zit in synergie.
              Daarom combineer ik microbiële inzichten met plantgenetica om robuuste systemen te ontwerpen.
            </li>
            <li>
              <strong>Onweerlegbaar bewijs:</strong> samen leidt dit tot een aanpak die verder gaat dan “saneren” of “productie”:
              we ontwerpen en bewijzen de installatie van een veerkrachtig, levend biologisch systeem.
            </li>
          </ul>
        </div>

        <div class="tab-panel" id="p4">
          <h3>Voor wie?</h3>
          <p class="muted">
            Ik werk onder meer voor:
          </p>
          <ul>
            <li>studie- en adviesbureaus (milieu, bodem, water, ecologie)</li>
            <li>bedrijven met site-, bodem- of waterdossiers</li>
            <li>landbouw- en landschapsprojecten die onderbouwing nodig hebben</li>
            <li>organisaties die bioproducten/bioremediatie in het veld willen verifiëren</li>
          </ul>
          <p class="muted">
            Twijfel je of jouw vraag past? Stuur me je context en ik zeg je snel wat een goede eerste stap is.
          </p>
          <p><a href="{{ '/contact/' | relative_url }}">Contacteer mij →</a></p>
        </div>

        <div class="tab-panel" id="p5">
          <h3>Artikels & lezingen</h3>
          <p class="muted">
            (Hier voeg je later makkelijk items toe. Start met 3–5 stuks, dat oogt meteen actief.)
          </p>
          <ul>
            <li><strong>Artikel:</strong> Titel — korte beschrijving (link)</li>
            <li><strong>Lezing:</strong> Event / organisatie — onderwerp (jaar)</li>
            <li><strong>Interview:</strong> Medium — topic (jaar)</li>
          </ul>
        </div>
      </div>
    </div>

    <div class="two-col">
      <div>
        <img src="{{ page.about_image_2 | relative_url }}" alt="Eco-GenX — landschap, bodem en natuurprocessen">
      </div>
      <div>
        <h3>Daarom Eco-GenX: Engineering Nature</h3>
        <p class="muted">
          Met deze visie heb ik Eco-GenX opgericht. Niet enkel om bodems “schoon” te maken,
          maar om landschappen weer <strong>gezond en productief</strong> te maken op een manier die wetenschappelijk robuust
          én economisch haalbaar is.
        </p>
        <p class="muted">
          Eco-GenX combineert natuur-gebaseerde technieken met diepgaand inzicht in microbiële gemeenschappen (MicroProof)
          en de selectie van robuust plantmateriaal (PlantIQ). Zo lever ik geen beloftes, maar resultaten waar je beslissingen op kan nemen.
        </p>
        <p class="muted">
          <strong>Waar staat Eco-GenX voor?</strong> “Eco” verwijst naar ecologie en het geheel van natuurlijke processen.
          “GenX” verwijst naar genetica en de meetbare “proof” laag (DNA/eDNA) waarmee we begrijpen wat er gebeurt — en bijsturen.
        </p>
      </div>
    </div>
  </section>

</div>
