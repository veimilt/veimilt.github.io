<section class="hero">
    <div class="hero-background">
        <img
            src="/images/kartta.webp"
            alt=""
            fetchpriority="high"
            width="1920"
            height="1080"
        />
    </div>
    <div class="container">
        <!-- TEXT BLOCK -->
        <div class="hero-content">
            <h1 class="hero-title">
                Jotta voit myydä julkiselle sektorille
                <span class="gradient-text">Tulee sinun tuntea se.</span>
            </h1>

            <p class="hero-description">
                Julkisen sektorin parhaat myyntimahdollisuudet piilevät
                kokouspöytäkirjoissa, päätöksissä sekä suunnitelmissa.
                Kokousvahti analysoi ne puolestasi ja toimittaa sinun alallesi
                sopivat mahdollisuudet suoraan sähköpostiisi.
            </p>

            <!-- CTA BUTTONS -->
            <div class="cta-buttons">
                <a class="herobutton" href="#">Tilaa esittelymateriaalit</a>
                <a class="herobutton" href="#"
                    >Varaa tapaaminen <svg
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
                    </svg></a
                >
            </div>

            <!-- <p class="disclaimer">
                Ei roskapostia, vain satunnaisia päivityksiä. Voit peruuttaa
                tilauksen milloin tahansa.
            </p> -->
        </div>

        <!-- DEMO CARD
        <div class="demo-section">
            <div class="demo-card">
                <div class="card-header">
                    <span class="badge">Reaaliaikainen projekti-yhteenveto</span
                    >
                    <span class="version">v1.0</span>
                </div>

                <div class="card-content">
                    <div class="project-status">
                        <div>
                            <p class="label">Nykyinen projekti</p>
                            <p class="project-name">
                                Uusi portfolio-verkkosivusto
                            </p>
                        </div>
                        <span class="status-badge"> Käynnissä </span>
                    </div>

                    <div class="stats-grid">
                        <div class="stat-item">
                            <p class="stat-label">Sivuja</p>
                            <p class="stat-value">8</p>
                        </div>
                        <div class="stat-item">
                            <p class="stat-label">Komponentteja</p>
                            <p class="stat-value">32</p>
                        </div>
                        <div class="stat-item">
                            <p class="stat-label">Aikaa säästetty</p>
                            <p class="stat-value">72%</p>
                        </div>
                    </div>

                    <div class="progress-bar">
                        <div class="progress-fill"></div>
                    </div>

                    <p class="progress-text">
                        Olet 90% edellä vastaavia projekteja.
                    </p>
                </div>
            </div>
        </div> -->
    </div>
</section>

<style>
    .hero {
        position: relative;
        width: 100%;
        padding: 3rem 0;
        background: linear-gradient(var(--bg-body), var(--bg-cta));
        min-height: 800px;
        overflow: hidden;
        z-index: 0;
    }

    .container {
        max-width: var(--container-xl);
        margin: 0 auto;
        padding: 0 1rem;
        z-index: 100;
        position: relative;
    }

    .hero-content {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        width: 100%;
        margin: 0 auto;
    }

    .hero-title {
        font-size: var(--text-4xl);
        line-height: var(--leading-tight);
        display: flex;
        flex-direction: column;
        text-align: center;
        width: 100%;
        color: var(--text-highcontrast);
        margin-bottom: 0;
        letter-spacing: normal;
        font-family:
            system-ui,
            -apple-system,
            BlinkMacSystemFont,
            "Segoe UI",
            Roboto,
            Oxygen,
            Ubuntu,
            Cantarell,
            "Open Sans",
            "Helvetica Neue",
            sans-serif;
    }

    .gradient-text {
        display: block;
        width: fit-content;
        margin: 0 auto;
        background: linear-gradient(
            to right,
            var(--text-gradient-start),
            var(--text-gradient-end)
        );
        -webkit-background-clip: text;
        background-clip: text;
        color: transparent;
    }

    .hero-description {
        margin-top: 1rem;

        max-width: 48rem;
        font-size: var(--text-lg);
        line-height: var(--leading-relaxed);
        color: var(--text-subtle);
        margin-bottom: 0;
    }

    .cta-buttons {
        margin-top: var(--space-5);
        display: flex;
        flex-direction: column-reverse;
        gap: 0.5rem;
        width: 100%;
    }

    
    /* 
    .disclaimer {
        margin-top: 1rem;
        font-size: var(--text-xs);
        color: var(--text-subtle);
        margin-bottom: 0;
    } */
    .hero-background {
        position: absolute;
        top: 150px;
        left: 0;
        width: 100%;
        height: 100%;
        z-index: 1;
        perspective: 850px;
        perspective-origin: 50% 50%;
        overflow: hidden;
        /* Important! */
        user-select: none;
    }

    .hero-background img {
        width: 100%;
        height: 120%;
        /* Make image taller than container */
        object-fit: cover;
        transform: rotateX(75deg) scale(1.1) translateY(0%);
        transform-origin: center;
        filter: opacity(0.5) brightness(0);
        animation: slide-vertical 7s ease-out forwards;
    }

    @keyframes slide-vertical {
        0% {
            transform: rotateX(75deg) scale(1.1) translateY(0%);
        }

        100% {
            transform: rotateX(80deg) scale(1.25) translateY(-25%);
        }
    }

    /* Tablet and up */
    @media (min-width: 640px) {
        .hero {
            padding: 4rem 0;
        }

        .hero-title {
            font-size: 3rem;
            line-height: 1.15;
        }

        .hero-description {
            margin-top: 1.5rem;
            font-size: var(--text-xl);
        }

        .cta-buttons {
            flex-direction: row;
            justify-content: center;
            gap: 0.75rem;
        }

        .herobutton {
            width: fit-content;
        }

        .hero-background {
            top: 150px;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 100;
            z-index: 1;
            transform: scale(1.25);
        }

        .hero-background img {
            width: 100%;
            height: 100%;
            object-fit: contain;
            object-position: center;
            transform: rotateX(70deg) scale(1.2) translateY(0);
            animation: slide-vertical 7s ease-out forwards;
        }

        @keyframes slide-vertical {
            0% {
                transform: rotateX(70deg) scale(1.2) translateY(0%);
            }

            100% {
                transform: rotateX(75deg) scale(1.4) translateY(-17%);
            }
        }
    }

    /* Desktop */
    @media (min-width: 768px) {
        .demo-section {
            flex-direction: row;
            align-items: stretch;
            justify-content: center;
        }
    }

    @media (min-width: 1024px) {
        .hero-title {
            font-size: 4rem;
        }

        .hero-background {
            top: -75px;
            left: 0;
            width: 100%;
            height: 150%;
            z-index: 100;
            perspective: 1000px;
            perspective-origin: 50% 50%;
            z-index: 1;
        }

        .hero-background img {
            width: 100%;
            height: 100%;
            object-fit: contain;
            object-position: center;
            transform: rotateX(65deg) scale(1.4) translateY(0);
            animation: slide-vertical 7s ease-out forwards;
        }

        @keyframes slide-vertical {
            0% {
                transform: rotateX(65deg) scale(1.4) translateY(0%);
            }

            100% {
                transform: rotateX(75deg) scale(1.7) translateY(-22%);
            }
        }
    }

    @media (min-width: 1236px) {
        .hero-background {
            top: -50px;
        }
    }
</style>
