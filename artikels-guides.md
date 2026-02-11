---
title: Artikels & guides
layout: default
permalink: /over/artikels-guides/
nav:
  order: 5
  tooltip: Artikels & guides
---

<style>
  /* =========================================================
     Artikels & guides — headerhoogte zoals "Voor wie"
     - zelfde compacte hero (niet te hoog)
     - zin onder titel verwijderd
     ========================================================= */

  main{ max-width:none !important; padding:0 !important; overflow:visible !important; }
  main > *, main .content, main article, main .page, main .post{
    max-width:none !important; padding:0 !important; margin:0 !important; overflow:visible !important;
  }

  /* hide default injected page title (theme-dependent) */
  .page-title,
  .page-header,
  .page-header h1,
  h1.page-title,
  main > h1:first-child{
    display:none !important;
  }

  .ag{
    --max: 1200px;
    --pad: 1.25rem;
    --cream: var(--eco-cream, #f6f4ee);
    --ink: rgba(0,0,0,.86);
    --muted: rgba(0,0,0,.66);
    --shadow: 0 14px 36px rgba(0,0,0,.06);
    --line: rgba(0,0,0,.10);
  }

  /* ✅ Compacte hero (zoals "Voor wie") */
  .hero{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    padding: 2.05rem 0 1.45rem; /* <- compacter */
    background: linear-gradient(180deg, rgba(11,59,47,.92), rgba(8,42,34,.92));
    color: rgba(255,255,255,.92);
    border-bottom: 1px solid rgba(0,0,0,.08);
  }
  .hero .inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
  }
  .eyebrow{
    font-size: .86rem;
    letter-spacing: .10em;
    text-transform: uppercase;
    opacity: .85;
    margin-bottom: .65rem;
  }
  .hero h1{
    margin:0;
    font-size: 2.35rem;
    line-height: 1.06;
    letter-spacing: .02em;
    max-width: 30ch;
  }

  .body{
    background: var(--cream);
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    padding: 2.2rem 0 3.2rem;
    border-top: 1px solid rgba(0,0,0,.06);
  }
  .body .inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
  }

  .grid{
    display:grid;
    grid-template-columns: 1.15fr .85fr;
    gap: 1.25rem;
    align-items: start;
  }

  .card{
    background: rgba(255,255,255,.62);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    box-shadow: var(--shadow);
    overflow:hidden;
  }
  .pad{ padding: 1.25rem 1.35rem; }

  .card h2{
    margin:0 0 .65rem;
    font-size: 1.45rem;
    color: var(--ink);
  }
  .card p{
    margin:0 0 .85rem;
    color: var(--muted);
    line-height: 1.75;
  }

  .item{
    padding: 1.05rem 1.15rem;
    border-top: 1px solid rgba(0,0,0,.08);
  }
  .item:first-child{ border-top: 0; }
  .item strong{ color: var(--ink); }
  .meta{ color: var(--muted); margin-top: .2rem; line-height: 1.55; }
  .item a{
    display:inline-block;
    margin-top: .45rem;
    text-decoration:none;
    font-weight:800;
    color: rgba(11,59,47,.92);
    border-bottom: 1px solid rgba(11,59,47,.35);
    padding-bottom: .06rem;
  }

  .imgbox{
    background: rgba(255,255,255,.72);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    overflow:hidden;
    box-shadow: var(--shadow);
  }
  .imgbox img{
    width:100%;
    height:auto;
    display:block;
  }
  .cap{
    padding: .85rem 1rem;
    color: var(--muted);
    line-height: 1.6;
    border-top: 1px solid rgba(0,0,0,.08);
  }

  @media (max-width: 980px){
    .grid{ grid-template-columns: 1fr; }
    .hero h1{ font-size: 2.0rem; }
  }
</style>

<div class="ag">

  <section class="hero">
    <div class="inner">
      <div class="eyebrow">Eco-GenX · Kennisbank</div>
      <h1>Artikels & guides</h1>
      <!-- ✅ zin verwijderd -->
    </div>
  </section>

  <section class="body">
    <div class="inner">

      <div class="grid">

        <div class="card">
          <div class="pad">
            <h2>Overzicht</h2>
            <p>Ik schreef mee aan volgende handleidingen, richtlijnen en blogposts.</p>
          </div>

          <div class="item">
            <strong>Code van goede praktijk (OVAM)</strong>
            <div class="meta">Richtlijnen / aanpak · </div>
            <a href="[https://example.com](https://ovam.vlaanderen.be/documents/177281/310282/Code+of+Good+Practice+-+Phytoremediation.pdf/4d4a087a-b543-25b1-77a1-14f932f1742e?version=1.0&t=1653496052399&download=true)">Open →</a>
          </div>

          <div class="item">
            <strong>Guide / Bodemleven in 1000 Limburgse tuinen </strong>
            <div class="meta">2024 · Bodemgezondheid · Bodemleven & activiteit in 1000 tuinen</div>
            <a href="[Rapport](https://archief.onderzoek.omgeving.vlaanderen.be/OMG_onderzoek_VPO-PBM_250201_1.2)">Open →</a>
          </div>

          <div class="item">
            <strong>Artikel / Scholen practica (placeholder)</strong>
            <div class="meta">2024 · Bodem-Practicum · 2e en 3e graad middelbaar bio</div>
            <a href="[Practicum bodemorganismen karakterisatie](https://www.klascement.net/downloadbaar-lesmateriaal/223909)">Open →</a>
          </div>

          <div class="item">
            <strong>Artikel / Scholen practica (placeholder)</strong>
            <div class="meta">2024 · DNA-Practicum · 2e en 3e graad middelbaar bio</div>
            <a href="[Practicum eDNA bodemleven](https://www.klascement.net/downloadbaar-lesmateriaal/223907))">Open →</a>
          </div>
          
        </div>

        <div class="imgbox">
          <!-- Upload je scan/screenshot hiernaartoe: /images/code-van-goede-praktijk.jpg -->
          <img src="{{ '/images/code-van-goede-praktijk.jpg' | relative_url }}" alt="Code van goede praktijk (OVAM)">
          <div class="cap">
          </div>
        </div>

      </div>

    </div>
  </section>

</div>
