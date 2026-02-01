<style>
  /* =======================================================
     Certified block (Home) — 2x2 grid zoals je voorbeeld
     ======================================================= */
  .cert-wrap{
    position: relative;
    left: 50%;
    right: 50%;
    width: 100vw;
    margin-left: -50vw;
    margin-right: -50vw;

    background: #fff;
    border-top: 1px solid rgba(0,0,0,.06);
    border-bottom: 1px solid rgba(0,0,0,.06);
  }

  .cert-grid{
    display: grid;
    grid-template-columns: 1fr 1fr;
  }

  .cert-cell{
    min-height: 360px;
  }

  .cert-photo{
    position: relative;
    overflow: hidden;
  }
  .cert-photo img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
  }

  .cert-text{
    padding: 3.2rem 3rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .cert-eyebrow{
    font-size: .85rem;
    letter-spacing: .10em;
    text-transform: uppercase;
    opacity: .75;
    margin-bottom: .75rem;
  }

  .cert-text h2{
    margin: 0 0 1rem;
    font-size: 1.9rem;
    line-height: 1.12;
  }

  .cert-text p{
    margin: 0 0 .9rem;
    line-height: 1.7;
    opacity: .86;
    max-width: 68ch;
  }

  .cert-link{
    margin-top: .6rem;
    font-weight: 600;
    text-decoration: none;
    color: rgba(11,59,47,.92);
    border-bottom: 1px solid rgba(11,59,47,.35);
    align-self: flex-start;
    padding-bottom: .08rem;
  }

  /* mobile */
  @media (max-width: 980px){
    .cert-grid{ grid-template-columns: 1fr; }
    .cert-text{ padding: 2.1rem 1.25rem; }
    .cert-cell{ min-height: unset; }
    .cert-photo{ height: 320px; }
  }
</style>

<section class="cert-wrap" aria-label="Gecertificeerde kwaliteit">
  <div class="cert-grid">

    <!-- 1) FOTO linksboven -->
    <div class="cert-cell cert-photo">
      <img src="{{ '/images/cert-1.jpg' | relative_url }}" alt="Staalnames en analytische kwaliteitsaanpak">
    </div>

    <!-- 2) TEKST rechtsboven -->
    <div class="cert-cell cert-text">
      <div class="cert-eyebrow">Gecertificeerde kwaliteitsaanpak</div>
      <h2>Meetbaar bewijs — decision-ready advies</h2>
      <p>
        Eco-GenX combineert veldwerk, labo en data om onzekerheid weg te nemen.
        Niet “mooie beloftes”, maar onderbouwde conclusies die je kan verdedigen —
        technisch én praktisch.
      </p>
      <p>
        Van staalname en interpretatie tot monitoring en bijsturing: je krijgt duidelijke
        stappen en een aanpak die reproduceerbaar is.
      </p>
      <a class="cert-link" href="{{ '/certificaten/' | relative_url }}">Bekijk certificaten →</a>
    </div>

    <!-- 3) TEKST linksonder -->
    <div class="cert-cell cert-text">
      <div class="cert-eyebrow">Analytische expertise</div>
      <h2>Kwaliteit die je project versnelt</h2>
      <p>
        Door slim te meten (multi-line-of-evidence) kan je sneller beslissen:
        wat werkt, waar zit het risico, en welke interventie levert het meeste effect.
      </p>
      <p>
        Ideaal voor bodemherstel, fytoremediatie, monitoring van natuurlijke attenuatie
        en verificatie van bio-claims.
      </p>
      <a class="cert-link" href="{{ '/contact/' | relative_url }}">Even sparren →</a>
    </div>

    <!-- 4) FOTO rechtsonder -->
    <div class="cert-cell cert-photo">
      <img src="{{ '/images/cert-2.jpg' | relative_url }}" alt="Laboratoriumanalyse en pipetteren">
    </div>

  </div>
</section>
