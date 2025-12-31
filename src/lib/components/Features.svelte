<section class="features">
    <div class="container">
        <div class="features-header">
            <h2 class="features-title">
                Kilpailutukset voittaa useimmiten taho, joka tunnetaan jo
                valmiiksi
            </h2>
        </div>

        <div class="intro-text">
            <p>
                Kokousvahti on suunniteltu yrityksille, jotka myyvät julkiselle
                sektorille ja haluavat pysyä ajan tasalla asiakkaidensa
                päätöksenteosta ja tulevista tarpeista. Pääasialliset
                asiakkaamme ovat rakennusalan toimijat, terveydenhuollon sekä
                hoiva-alan asiantuntijat sekä koulutus ja kulttuuriprojektien
                parissa työskentelevät tahot.
            </p>
        </div>
        <div class="features-grid">
            <div class="feature-card">
                <div class="card-icon">
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="none"
                        stroke="currentColor"
                        stroke-width="2"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                    >
                        <path d="M21 5H3"></path>
                        <path d="M10 12H3"></path>
                        <path d="M10 19H3"></path>
                        <circle cx="17" cy="15" r="3"></circle>
                        <path d="m21 19-1.9-1.9"></path>
                    </svg>
                </div>
                <div class="card-header">
                    <h3 class="card-title">
                        Tekoälyagentti vahtii puolestasi 24/7
                    </h3>
                </div>
                <div class="card-content">
                    <p>
                        Kielimallipohjainen agentti lukee julkisen sektorin
                        kokouspöytäkirjoja 24/7 ja tunnistaa sinun toimialallesi
                        sopivat myyntimahdollisuudet, hankinnat ja projektit.
                    </p>
                </div>
            </div>

            <div class="feature-card">
                <div class="card-icon">
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="none"
                        stroke="currentColor"
                        stroke-width="2"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                    >
                        <path
                            d="M10 20a1 1 0 0 0 .553.895l2 1A1 1 0 0 0 14 21v-7a2 2 0 0 1 .517-1.341L21.74 4.67A1 1 0 0 0 21 3H3a1 1 0 0 0-.742 1.67l7.225 7.989A2 2 0 0 1 10 14z"
                        ></path>
                    </svg>
                </div>
                <div class="card-header">
                    <h3 class="card-title">Ei valtavia määriä turhaa dataa</h3>
                </div>
                <div class="card-content">
                    <p>
                        Tekoälykielimallit ovat fiksumpia kuin usein käytetyt
                        sanahakuun perustuvat ratkaisut. Löydämme tiiviisti
                        juuri sinulle relevantit tiedot ilman loputtomia
                        listoja.
                    </p>
                </div>
            </div>

            <div class="feature-card">
                <div class="card-icon">
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="none"
                        stroke="currentColor"
                        stroke-width="2"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                    >
                        <path d="M16 5H3"></path>
                        <path d="M16 12H3"></path>
                        <path d="M11 19H3"></path>
                        <path d="m15 18 2 2 4-4"></path>
                    </svg>
                </div>
                <div class="card-header">
                    <h3 class="card-title">Säännöllinen raportointi</h3>
                </div>
                <div class="card-content">
                    <p>
                        Saat viikoittain juuri sinun yrityksellesi olennaiset
                        havainnot sekä toimenpide-ehdotukset selkeässä muodossa
                        suoraan sähköpostiin.
                    </p>
                </div>
            </div>
        </div>
    </div>
</section>

<style>
    .features {
        width: 100%;
        padding: 4rem 0;
        background-color: var(--accent-bg-brown);
    }

    .container {
        max-width: var(--container-xl);
        margin: 0 auto;
        padding: 0 1rem;
    }

    .features-header {
        display: flex;
        flex-direction: column;
        gap: 1rem;
        margin-bottom: 1.5rem;
        margin-left: 0.5rem;
    }

    .features-title {
        width: 100%;
        font-size: var(--headings-mobile);
        font-weight: 600;
        line-height: var(--leading-tight);
        color: var(--text-highcontrast);
    }

    .features-grid {
        display: grid;
        gap: 1.5rem;
        grid-template-columns: 1fr;
        padding-top: 3rem;
    }

    .intro-text {
        position: relative;
        grid-column: 1 / -1;
        margin-left: 0.5rem;
    }

    .intro-text p {
        font-size: var(--text-lg);
        line-height: var(--leading-relaxed);
        color: var(--text-subtle);
        max-width: 64rem;
        margin: 0;
    }

    .feature-card {
        position: relative;
        background: var(--card-bg-primary);
        padding: 2rem;
        padding-top: 1.5rem;
        padding-bottom: 2.5rem;
        box-shadow: var(--shadow-smooth-strong);
        display: flex;
        flex-direction: column;
        justify-content: center;
        max-width: 500px;
        margin: 0 auto;
        border-radius: var(--radius-primary);
        border: 1px solid var(--color-border);
        min-height: 333px;
    }

    .card-icon {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 48px;
        height: 48px;
        border-radius: var(--radius-full);
        background-color: var(--bg-primary-subtle);
        color: var(--icon-primary);
        margin-bottom: 1rem;
        flex-shrink: 0;
    }

    .card-header {
        margin-bottom: 1rem;
    }

    .card-title {
        font-size: var(--text-2xl);
        font-weight: 600;
        line-height: var(--leading-tight);
        color: var(--text-highcontrast);
        margin: 0;
    }

    .card-content {
        display: flex;
        flex-direction: column;
        gap: 0.75rem;
        flex-grow: 1;
    }

    .card-content p {
        font-size: var(--text-base);
        line-height: var(--leading-relaxed);
        color: var(--text-subtle);
        margin: 0;
    }

    /* Tablet and up */
    @media (min-width: 640px) {
        .features-grid {
            grid-template-columns: repeat(2, 1fr);
        }
    }

    /* Desktop */
    @media (min-width: 768px) {
        .features-title {
            font-size: var(--headings-tablet);
        }

        .card-content p {
            line-height: var(--leading-relaxed);
            margin: 0;
        }

        .card-icon {
            width: 56px;
            height: 56px;
        }

        .card-icon svg {
            width: 28px;
            height: 28px;
        }

        .feature-card {
            padding: 2.5rem;
            padding-top: 2rem;
            padding-bottom: 3rem;
        }

        .intro-text {
            grid-column: 1 / -1;
            margin-top: 2rem;
        }
    }

    @media (min-width: 1024px) {
        .features {
            padding: 7rem 0;
            padding-bottom: 8rem;
        }

        .features-title {
            font-size: var(--headings-laptop);
        }

        .intro-text p {
            font-size: var(--text-xl);
        }

        .container {
            padding: 0 2rem;
        }
        .features-grid {
            grid-template-columns: repeat(3, 1fr);
            padding-top: 4rem;
        }
    }
</style>
