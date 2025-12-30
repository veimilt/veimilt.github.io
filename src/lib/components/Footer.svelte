<script>
    const year = new Date().getFullYear();
</script>

<footer>
    <div class="container">
        <div class="footer-content">
            <div class="footer-branding">
                <div class="brand-logo">
                    <img
                        src="/images/kokousvahti_logo.webp"
                        alt="kokousvahti logo"
                    />
                </div>
                <p class="brand-description">
                    Seuraa julkisen sektorin päätöksentekoa ja tunnista
                    myyntimahdollisuudet tekoälyavusteisen analyysin avulla.
                </p>
            </div>

            <div class="footer-links">
                <div class="link-column">
                    <div class="column-title">Tuote</div>
                    <ul>
                        <li><a href="/terveydenhuolto">Terveydenhuolto</a></li>
                        <li><a href="/rakennusala">Rakennusala</a></li>
                    </ul>
                </div>

                <div class="link-column">
                    <div class="column-title">Yritys</div>
                    <ul>
                        <li><a href="/contact">Yhteystiedot</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

    <hr class="separator" />

    <div class="container container-footer-bottom">
        <div class="footer-bottom">
            <div class="disclaimer-section-1">
                <h3 class="disclaimer-title">Vastuuvapautuslauseke</h3>
                <p class="disclaimer-text">
                    Tämä palvelu tarjoaa automaattisesti luotuja yhteenvetoja ja
                    analyyseja julkisen sektorin kokousdatasta. Vaikka pyrimme
                    tarjoamaan mahdollisimman tarkkaa ja luotettavaa tietoa,
                    emme voi taata kaikkien tietojen virheettömyyttä tai
                    täydellisyyttä.
                </p>
                <p class="disclaimer-text">
                    Palvelu käyttää tekoälyä (LLM) tiedon käsittelyssä, mikä voi
                    johtaa tulkintavirheisiin tai epätarkkuuksiin. Käyttäjä on
                    itse vastuussa palvelun tuottaman tiedon käytöstä ja sen
                    perusteella tehdyistä päätöksistä.
                </p>
                <p class="disclaimer-text">
                    Emme vastaa mistään välittömistä tai välillisistä
                    vahingoista, jotka saattavat aiheutua palvelun käytöstä tai
                    sen tuottaman tiedon perusteella tehdyistä päätöksistä.
                    Suosittelemme aina tarkistamaan kriittiset tiedot
                    alkuperäisistä lähteistä.
                </p>
                <p class="disclaimer-text">
                    Pidätämme oikeuden muuttaa palvelun sisältöä ja
                    toiminnallisuuksia ilman erillistä ilmoitusta.
                </p>
            </div>
            <div class="disclaimer-section-2">
                <h3 class="disclaimer-title">Tekijänoikeudet</h3>
                <p class="copyright">
                    © {year} Kokousvahti. Kaikki oikeudet pidätetään. Palvelun sisältö
                    ja raportit on tarkoitettu vain tilaajien käyttöön.
                </p>
            </div>
        </div>
    </div>
    <div class="footer-branding-large">
        <h2 class="large-text">Kokousvahti</h2>
    </div>
</footer>

<style>
    footer {
        width: 100%;
        border-top: 1px solid var(--color-border);
        background-color: var(--bg-footer);
    }

    .container {
        max-width: var(--container-xl);
        margin: 0 auto;
        padding: 4rem 2rem;
    }

    .footer-content {
        display: flex;
        flex-direction: column;
        gap: 3rem;
    }

    .footer-branding {
        display: flex;
        flex-direction: column;
        gap: 0.75rem;
    }

    .brand-logo {
        height: 100px;
        object-fit: contain;
        overflow: hidden;
        display: flex;
        align-items: center;
        transform: translateX(-20px) translateY(-35px);
    }

    .brand-logo img {
        width: 200px;
    }

    .brand-description {
        max-width: 28rem;
        font-size: var(--text-smaller);
        line-height: var(--leading-relaxed);
        color: var(--text-subtle);
        margin: 0;
        transform: translateY(-50px);
    }

    .footer-links {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 3rem;
        font-size: var(--text-sm);
    }

    .link-column {
        display: flex;
        flex-direction: column;
        gap: 0.5rem;
    }

    .column-title {
        font-size: var(--text-sm);
        font-weight: 600;
        text-transform: uppercase;
        letter-spacing: 0.05em;
        color: var(--text-highcontrast);
    }

    .link-column ul {
        list-style: none;
        padding: 0;
        margin: 0;
        display: flex;
        flex-direction: column;
        gap: 0.25rem;
    }

    .link-column li {
        margin: 0;
    }

    .link-column a {
        color: var(--text-subtle);
        text-decoration: none;
    }

    .link-column a:hover {
        color: var(--text-highcontrast);
        text-decoration: underline;
    }

    .separator {
        margin: 0;
        border: none;
        border-top: 1px solid var(--color-border);
    }

    .footer-bottom {
        display: flex;
        flex-direction: column;
        gap: 2rem;
    }

    .disclaimer-section-1,
    .disclaimer-section-2 {
        width: 100%;
        display: flex;
        flex-direction: column;
        gap: 1.5rem;
        font-size: var(--text-sm);
    }

    .disclaimer-title {
        font-size: var(--text-base);
        font-weight: 600;
        color: var(--text-highcontrast);
        margin: 1rem 0 0 0;
    }

    .disclaimer-text,
    .copyright {
        line-height: var(--leading-relaxed);
        color: var(--text-subtle);
        margin: 0;
        width: 100%;
        max-width: 1000px;
    }

    .copyright {
        color: var(--text-subtle);
        margin: 0;
    }

    .footer-branding-large {
        width: 100%;
        overflow: hidden;
        padding: 3rem 0 2rem 0;
        position: relative;
    }

    .large-text {
        font-size: clamp(4rem, 15vw, 15rem);
        font-weight: 800;
        line-height: 1;
        color: var(--text-highcontrast);
        text-align: center;
        margin: 0;

        /* Cool shadow effect fading from top */
        background: var(--bg-footer-branding-text);
        -webkit-background-clip: text;
        background-clip: text;
        -webkit-text-fill-color: transparent;
        letter-spacing: normal;

        /* Additional shadow for depth */
    }

    /* Tablet and up */
    @media (min-width: 768px) {
        .footer-content {
            flex-direction: row;
            align-items: flex-start;
            justify-content: space-between;
            padding: 0 1rem;
        }

        .footer-links {
            grid-template-columns: repeat(2, 1fr);
        }
    }

    @media (min-width: 1024px) {
        .footer-content {
            flex-direction: row;
            align-items: flex-start;
            justify-content: space-between;
        }
        .container-footer-bottom {
            padding-top: 2rem;
        }
        .footer-bottom {
            gap: 2rem;
            justify-content: space-between;
            padding-left: 1rem;
            margin: 0 auto;
        }
    }
</style>
