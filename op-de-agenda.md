---
title: Op de agenda
layout: default
permalink: /over/op-de-agenda/
nav:
  order: 4
  tooltip: Op de agenda
---

<style>
  /* =========================================================
     Op de agenda — intro + agenda (clean)
     ========================================================= */

  main{ max-width:none !important; padding:0 !important; overflow:visible !important; }
  main > *, main .content, main article, main .page, main .post{
    max-width:none !important; padding:0 !important; margin:0 !important; overflow:visible !important;
  }

  .agendaPage{
    --max: 1200px;
    --pad: 1.25rem;
    --cream: var(--eco-cream, #f6f4ee);
    --ink: rgba(0,0,0,.86);
    --muted: rgba(0,0,0,.66);
    --line: rgba(0,0,0,.10);
    --shadow: 0 14px 36px rgba(0,0,0,.06);
  }

  /* compact hero (niet te hoog) */
  .hero{
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    background: linear-gradient(180deg, rgba(11,59,47,.92), rgba(8,42,34,.92));
    color: rgba(255,255,255,.92);
    padding: 1.7rem 0 1.2rem;
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
    margin-bottom: .5rem;
  }
  .hero h1{
    margin:0;
    font-size: 2.1rem;
    line-height: 1.08;
  }

  .body{
    background: var(--cream);
    position: relative;
    left: 50%; right: 50%;
    width: 100vw;
    margin-left: -50vw; margin-right: -50vw;

    padding: 1.6rem 0 3.2rem;
    border-top: 1px solid rgba(0,0,0,.06);
  }
  .body .inner{
    max-width: var(--max);
    margin: 0 auto;
    padding: 0 var(--pad);
  }

  /* intro paragraaf (lezingen-tekst) */
  .intro{
    background: rgba(255,255,255,.62);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    box-shadow: var(--shadow);
    padding: 1.1rem 1.25rem;
    color: var(--muted);
    line-height: 1.75;
  }
  .intro strong{ color: var(--ink); }

  /* agenda panel */
  .panel{
    margin-top: 1rem;
    background: rgba(255,255,255,.62);
    border: 1px solid rgba(0,0,0,.08);
    border-radius: 18px;
    box-shadow: var(--shadow);
    overflow:hidden;
  }
  .panelhead{
    display:flex;
    justify-content: space-between;
    align-items: baseline;
    gap: 1rem;
    padding: 1.05rem 1.25rem;
    border-bottom: 1px solid rgba(0,0,0,.08);
  }
  .panelhead strong{
    letter-spacing: .10em;
    text-transform: uppercase;
    font-size: .95rem;
    color: var(--ink);
  }
  .panelhead span{ color: var(--muted); }

  .list{
    padding: 1rem 1.05rem 1.2rem;
    display:flex;
    flex-direction: column;
    gap: .9rem;
  }

  .item{
    display:grid;
    grid-template-columns: 11rem 1fr;
    gap: 1rem;
    padding: .95rem 1rem;
    border-radius: 16px;
    background: rgba(255,255,255,.74);
    border: 1px solid rgba(0,0,0,.08);
  }
  .date{
    font-weight: 900;
    color: rgba(0,0,0,.82);
    letter-spacing: .02em;
    white-space: nowrap;
  }
  .main{
    display:flex;
    flex-direction: column;
    gap: .12rem;
    min-width: 0;
  }
  .title{
    font-weight: 900;
    color: var(--ink);
    line-height: 1.25;
  }
  .meta{
    color: var(--muted);
    line-height: 1.55;
  }
  .link{
    margin-top: .25rem;
    align-self: flex-start;
    text-decoration:none;
    font-weight: 900;
    color: rgba(11,59,47,.92);
    border-bottom: 1px solid rgba(11,59,47,.35);
    padding-bottom: .06rem;
  }

  .cta{
    margin-top: 1.05rem;
    background: rgba(11,59,47,.92);
    color: rgba(255,255,255,.92);
    border: 1px solid rgba(255,255,255,.12);
    border-radius: 18px;
    padding: 1.05rem 1.2rem;
  }
  .cta a{
    color: rgba(255,255,255,.92);
    text-decoration:none;
    border-bottom: 1px solid rgba(255,255,255,.35);
    padding-bottom: .08rem;
    font-weight: 900;
  }

  @media (max-width: 980px){
    .item{ grid-template-columns: 1fr; }
    .date{ white-space: normal; }
    .hero h1{ font-size: 1.85rem; }
  }
</style>

<div class="agendaPage">

  <section class="hero">
    <div class="inner">
      <div class="eyebrow">Eco-GenX · Lezingen & symposia</div>
      <h1>Op de agenda</h1>
    </div>
  </section>

  <section class="body">
    <div class="inner">

      <!-- ✅ KORTE LEZINGEN-TEKST BOVEN DE AGENDA -->
      <div class="intro">
        <strong>Ik geef lezingen en Q&amp;A’s</strong> (bv. PFAS/bodem/water, nature-based oplossingen, monitoring en interpretatie).
        Altijd zonder jargon, met correcte nuance en vertaald naar “wat betekent dit concreet?”.
        Wil je een sessie op jouw locatie? <a href="{{ '/contact/' | relative_url }}">Contacteer mij →</a>
      </div>

      <!-- ✅ AGENDA MET DATA -->
      <div class="panel">
        <div class="panelhead">
          <strong>Agenda</strong>
          <span>pas aan / voeg regels toe</span>
        </div>

        <div class="list">

          <!-- COPY/PASTE dit blok voor extra events -->
          <div class="item">
            <div class="date">11 feb 2026</div>
            <div class="main">
              <div class="title">Lezing Ronse</div>
              <div class="meta">19:30 · Ronse · PFAS proeftuin met hennep &amp; meetdata — interpretatie en vragen</div>
              <a class="link" href="[link](https://www.facebook.com/events/1301792891756724/)">Info / inschrijven →</a>
            </div>
          </div>

          <div class="item">
            <div class="date">19 mrt 2026</div>
            <div class="main">
              <div class="title">Teachup!2030</div>
              <div class="meta">9:00 · Herman Teirlinck Brussel ·  Workshop "Grondig leren: ontdek het belang van een gezonde bodem"</div>
              <a class="link" href="link](https://www.linkedin.com/feed/update/urn:li:activity:7424050690836262912/)">Eventpagina →</a>
            </div>
          </div>

          <div class="item">
            <div class="date">—</div>
            <div class="main">
              <div class="title">Boekbaar op aanvraag</div>
              <div class="meta">Gemeenten, burgergroepen, verenigingen · onderwerp op maat</div>
              <a class="link" href="{{ '/contact/' | relative_url }}">Vraag een lezing aan →</a>
            </div>
          </div>

        </div>
      </div>

      <div class="cta">
        Wil je dit op jouw locatie? <a href="{{ '/contact/' | relative_url }}">Contacteer mij →</a>
      </div>

    </div>
  </section>

</div>
