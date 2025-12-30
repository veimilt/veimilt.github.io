<script>
    let notifications = [
        {
            id: 1,
            title: "Uusi tarjousmahdollisuus",
            location: "Helsinki",
            category: "Terveydenhuolto",
        },
        {
            id: 2,
            title: "Rakennusprojekti käynnistyy",
            location: "Tampere",
            category: "Infrastruktuuri",
        },
        {
            id: 3,
            title: "Uusi hankinta päätetty",
            location: "Vantaa",
            category: "Hoivapalvelut",
        },
    ];
</script>

<section class="hero">
    <div class="container">
        <div class="hero-content">
            <h1 class="hero-title">
                <span class="heading-main">
                    Jotta voit myydä julkiselle sektorille,
                </span>
                <span class="gradient-text"> Tulee sinun tuntea se. </span>
            </h1>

            <p class="hero-description">
                Julkisen sektorin parhaat myyntimahdollisuudet piilevät
                kokouspöytäkirjoissa, päätöksissä sekä suunnitelmissa.
                Kokousvahti analysoi ne puolestasi ja toimittaa sinun alallesi
                sopivat mahdollisuudet suoraan sähköpostiisi.
            </p>

            <div class="herobuttons">
                <a
                    class="herobutton"
                    href="https://calendar.app.google/KB5ZkR7cQvuc31pt8"
                >
                    Tilaa esittelymateriaalit
                </a>
                <a
                    class="herobutton"
                    href="https://calendar.app.google/KB5ZkR7cQvuc31pt8"
                >
                    Varaa tapaaminen
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
            </div>
        </div>
    </div>
    <div class="hero-visual">
        <div class="map-container">
            <img src="/images/kartta.webp" alt="Suomen kartta" />
        </div>

        <div class="notifications">
            {#each notifications as notification, index}
                <div class="notification">
                    <div class="notification-header">
                        <span class="notification-badge"
                            >{notification.category}</span
                        >
                    </div>
                    <h3 class="notification-title">{notification.title}</h3>
                    <p class="notification-location">
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            width="14"
                            height="14"
                            viewBox="0 0 24 24"
                            fill="none"
                            stroke="currentColor"
                            stroke-width="2"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                        >
                            <path
                                d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z"
                            ></path>
                            <circle cx="12" cy="10" r="3"></circle>
                        </svg>
                        {notification.location}
                    </p>
                </div>
            {/each}
        </div>
    </div>
</section>

<style>
    .hero {
        position: relative;
        width: 100%;
        background: var(--bg-hero);
        overflow: hidden;
    }

    .container {
        position: relative;
        max-width: 1500px;
        margin: 0 auto;
        padding: 0 1rem;
        z-index: 2;
    }

    .hero-content {
        display: flex;
        flex-direction: column;
        width: 100%;
        padding-top: 2.5rem;
    }

    .hero-title {
        font-size: 2.5rem;
        line-height: var(--leading-tight);
        display: flex;
        flex-direction: column;
        color: var(--text-highcontrast);
        margin-bottom: 0;
    }

    .gradient-text {
        display: block;
        background: linear-gradient(
            to right,
            var(--text-gradient-start),
            var(--text-gradient-end)
        );
        -webkit-background-clip: text;
        background-clip: text;
        color: transparent;
        width: fit-content;
    }

    @keyframes fadeUp {
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }

    .hero-description {
        margin-top: 1.5rem;
        max-width: 750px;
        font-size: var(--text-lg);
        line-height: var(--leading-relaxed);
        color: var(--text-subtle);
        margin-bottom: 0;
    }

    .herobuttons {
        margin-top: 1.75rem;
        display: flex;
        flex-direction: column-reverse;
        gap: 0.75rem;
        width: 100%;
    }

    .herobutton {
        width: 100%;
        margin: 0 auto;
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
        transition: var(--transition-fast);
        box-shadow: var(--shadow-md);
    }

    .herobutton:hover {
        background: var(--button-bg-hover);
    }

    .herobutton svg {
        transition: transform var(--transition-base);
    }

    .herobutton:hover svg {
        transform: translateX(4px);
    }

    .hero-visual {
        position: relative;
        width: 100%;
        min-height: 400px;
        max-width: 700px;
        margin: 0 auto;
        z-index: 1;
    }

    .hero-visual p,
    .hero-visual h3 {
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

    .map-container {
        position: absolute;
        inset: 0;
        pointer-events: none;
        padding: 1rem;
    }

    .map-container img {
        width: 100%;
        height: 100%;
        /*  */
        object-fit: contain;
        /*  */
        object-position: left bottom;
        opacity: 0.5;
    }

    .notifications {
        position: relative;
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        gap: 1rem;
        padding: 2rem 1rem;
        max-width: 1536px;
        margin: 0 auto;
    }

    .notification {
        border: 1px solid var(--border-subtle);
        border-radius: 1rem;
        padding: 1rem;
        background-color: var(--bg-notification);
        backdrop-filter: blur(50px);
        opacity: 0;
        transform: translateY(25px) scale(0.5);
        animation: slideIn 0.3s cubic-bezier(0.165, 0.84, 0.44, 1) forwards;
        width: 65%;
        max-width: 500px;
        will-change: transform;
    }

    .notification:nth-child(2) {
        animation-delay: 0.25s;
    }
    .notification:nth-child(3) {
        animation-delay: 0.5s;
    }

    @keyframes slideIn {
        to {
            opacity: 1;
            transform: translateY(0) scale(1);
        }
    }
    .notification-header {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-bottom: 0.5rem;
        letter-spacing: normal;
    }

    .notification-badge {
        font-size: var(--text-xs);
        font-weight: 600;
        padding: 0.25rem 0.75rem;
        border-radius: 9999px;
        background: var(--color-primary-hover);
        color: white;
    }

    .notification-title {
        font-size: var(--text-base);
        font-weight: 600;
        color: var(--text-highcontrast);
        margin: 0 0 0.5rem 0;
    }

    .notification-location {
        display: flex;
        align-items: center;
        gap: 0.25rem;
        font-size: var(--text-sm);
        color: var(--text-subtle);
        margin: 0;
    }

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

        .herobuttons {
            flex-direction: row;
        }

        .herobutton {
            width: fit-content;
            margin: 0;
        }

        .hero-visual {
            min-height: 500px;
        }
    }

    @media (min-width: 1024px) {
        .hero {
            padding: 6rem 0;
        }

        .hero-description {
        }
        .container {
            padding: 0;
        }

        .hero-content {
            max-width: 600px;
            padding-left: 2rem;
        }

        .hero-visual {
            position: absolute;
            top: 0;
            right: 0;
            width: 50%;
            height: 100%;
            max-width: none;
            max-height: none;
            margin: 0;
        }

        /* .hero-visual::after {
            position: absolute;
            content: "";
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        } */

        .notifications {
            justify-content: center;
            height: 100%;
            padding-left: 10rem;
        }

        .notification:nth-child(1) {
            animation-delay: 0.5s;
        }
        .notification:nth-child(2) {
            animation-delay: 0.75s;
        }
        .notification:nth-child(3) {
            animation-delay: 1s;
        }

        .notification {
            width: 400px;
        }
    }

    @media (min-width: 1280px) {
        .hero {
            min-height: 900px;
        }

        .hero-content {
            max-width: none;
            padding-top: 3rem;
        }

        .hero-title {
            font-size: 4rem;
        }

        .notifications {
            align-items: center;
            padding-top: 4rem;
        }
    }
    @media (min-width: 1400px) {
        .hero-visual .map-container img {
            object-position: center;
        }
        .notifications {
            align-items: center;
        }
        .notifications {
            align-items: flex-start;
        }
    }
</style>
