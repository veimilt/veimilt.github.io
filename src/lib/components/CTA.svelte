<section class="cta-section">
    <div class="background-texture">
        <!-- <svg
            viewBox="0 0 1440 320"
            preserveAspectRatio="none"
            class="texture-svg"
        >
            <defs>
                <linearGradient
                    id="fadeGradient"
                    x1="0%"
                    y1="100%"
                    x2="0%"
                    y2="0%"
                >
                    <stop
                        offset="0%"
                        style="stop-color:currentColor;stop-opacity:0.15"
                    />
                    <stop
                        offset="100%"
                        style="stop-color:currentColor;stop-opacity:0"
                    />
                </linearGradient>
            </defs>
            <path
                fill="url(#fadeGradient)"
                d="M0,96L48,112C96,128,192,160,288,176C384,192,480,192,576,170.7C672,149,768,107,864,101.3C960,96,1056,128,1152,138.7C1248,149,1344,139,1392,133.3L1440,128L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"
            ></path>
            <path
                fill="url(#fadeGradient)"
                d="M0,224L48,213.3C96,203,192,181,288,186.7C384,192,480,224,576,234.7C672,245,768,235,864,213.3C960,192,1056,160,1152,160C1248,160,1344,192,1392,208L1440,224L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"
            ></path>
        </svg> -->
    </div>

    <div class="container">
        <div class="cta-card">
            <div class="cta-content">
                <h2 class="cta-title">
                    Ruvetaanko töihin?<br>Suomen suurimmat yritykset luottavat
                    meihin.
                </h2>
                <p class="cta-description">
                    Olemme jo ansainneet Suomen suurimpien IT-, hoiva- ja
                    terveydenhuoltoalan sekä rakennusalan yritysten
                    luottamuksen. Näe itse, miten Kokousvahti auttaa sinua
                    pysymään askeleen edellä kilpailijoitasi.
                </p>
                <div class="cta-actions">
                    <a class="cta-button" href="https://calendar.app.google/KB5ZkR7cQvuc31pt8">
                        Aloita pilotti
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            width="20"
                            height="20"
                            viewBox="0 0 24 24"
                            fill="none"
                            stroke="currentColor"
                            stroke-width="2"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                        >
                            <path d="M5 12h14"></path>
                            <path d="m12 5 7 7-7 7"></path>
                        </svg>
                    </a>
                    <a class="cta-button" href="https://calendar.app.google/KB5ZkR7cQvuc31pt8">Tilaa esittelymateriaalit</a>
                </div>
                <p class="cta-footnote">
                    <span>✓ Nopea käyttöönotto</span>
                    <span>✓ Ei pitkää sitoutumista</span>
                    <span>✓ Suomalainen tuki</span>
                </p>
            </div>
        </div>
    </div>
</section>

<style>
    .cta-section {
        position: relative;
        width: 100%;
        padding: 4rem 0;
        overflow: hidden;
        background-image: linear-gradient(var(--bg-primary), var(--bg-cta));
        /* background-image: linear-gradient(rgba(127, 166, 230, 0.05)); */
    }

    .background-texture {
        position: absolute;
        bottom: 0;
        left: 0;
        right: 0;
        height: 100%;
        pointer-events: none;
        z-index: 0;
    }

    .container {
        position: relative;
        z-index: 1;
        max-width: var(--container-xl);
        margin: 0 auto;
        padding: 0 1rem;
    }

    .cta-card {
        position: relative;
        max-width: 56rem;
        margin: 0 auto;
        background-color: var(--bg-cta-card);
        border: 1px solid var(--border-cta-card);
        overflow: hidden;
        border-radius: 2rem;
        box-shadow: var(--shadow-cta);
    }

    .cta-content {
        padding: 3rem 1rem;
        padding-top: 2.5rem;
        text-align: center;
        position: relative;
        z-index: 2;
    }

    .cta-title {
        font-size: 1.75rem;
        font-weight: 700;
        line-height: var(--leading-tight);
        color: var(--text-highcontrast);
        margin: 0 0 1.5rem 0;
        line-height: 1.1;
    }

    .cta-description {
        font-size: var(--text-lg);
        line-height: var(--leading-relaxed);
        color: var(--text-highcontrast);
        max-width: 42rem;
        margin: 0 auto;
    }

    .cta-actions {
        display: flex;
        flex-direction: column;
        gap: 0.75rem;
        align-items: center;
        justify-content: center;
        margin-bottom: 1.5rem;
        padding-top: 1.5rem;
    }

    .cta-button {
        width: 100%;
        display: inline-flex;
        align-items: center;
        justify-content: center;
        gap: 0.5rem;
        padding: var(--button-padding);
        font-weight: 600;
        font-size: var(--text-base);
        border-radius: var(--radius-full);
        cursor: pointer;
        background: var(--button-bg);
        color: white;
        transition: background-color var(--transition-fast);
        box-shadow: var(--shadow-md);
    }

    .cta-button:hover {
        background: var(--button-bg-hover);
    }

    .cta-footnote {
        font-size: var(--text-sm);
        color: var(--text-subtle);
        margin: 0;
        line-height: var(--leading-relaxed);
        display: flex;
        gap: 0.5rem;
        flex-direction: column;
        justify-content: center;
        margin: 0 auto;
    }

    /* Tablet and up */
    @media (min-width: 640px) {
        .cta-title {
            font-size: var(--headings-tablet);
        }
        .cta-actions {
            flex-direction: row;
            gap: 1rem;
        }

        .cta-button {
            width: auto;
        }
    }

    /* Desktop */
    @media (min-width: 768px) {
        .cta-footnote {
            display: flex;
            gap: 1rem;
            flex-direction: row;
        }
    }

    /* Large desktop */
    @media (min-width: 1024px) {
        .cta-section {
            padding: 7rem 0;
            padding-bottom: 5rem;
        }

        .cta-content {
            padding: 3rem;
            padding-top: 2.5rem;
        }
        .cta-title {
            font-size: var(--headings-laptop);
        }

        .cta-actions {
            padding-top: 2rem;
        }
    }
</style>
