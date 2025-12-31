<script>
    import { onMount } from "svelte";
    let { data } = $props();

    let puh = $state("");

    onMount(() => {
        const parts = ["MDQ2N", "CA1ODU", "gMD", "QgODU", "zKw=="];
        puh = atob(parts.join(""));
    });
</script>

<section class="contact">
    <div class="container">
        <h1>Ota meihin yhteyttä:</h1>
        <div class="contact-content">
            <div class="contact-info">
                <div class="info-items">
                    <div class="info-item">
                        <span class="label">Sähköposti</span>
                        <a href="mailto:{data.email}">{data.email}</a>
                    </div>

                    <div class="info-item">
                        <span class="label">Osoite</span>
                        <span>{data.address}</span>
                    </div>

                    <div class="info-item">
                        <span class="label">Puhelin</span>
                        <a
                            href="tel:{puh
                                .split('')
                                .reverse()
                                .join('')
                                .replace(/\s/g, '')}"
                        >
                            <span class="puh-reverse">{puh}</span>
                        </a>
                    </div>

                    <div class="info-item">
                        <span class="label">Y-tunnus</span>
                        <span>{data.ytunnus}</span>
                    </div>
                </div>
            </div>

            <div class="contact-image">
                <img
                    src="/images/kokousvahti.webp"
                    alt="kokousvahti contact"
                    width="1024"
                    height="1024"
                />
            </div>
        </div>
    </div>
</section>

<style>
    .contact {
        padding: clamp(2rem, 4vw, 4rem) clamp(1rem, 5vw, 2rem);
        background-color: var(--bg-primary);
        /* background-image: linear-gradient(var(--bg-primary), var(--bg-cta)); */
    }

    h1 {
        color: var(--text-highcontrast);
        margin: 3rem 0;
    }

    .contact-content {
        display: flex;
        gap: 1rem;
        flex-wrap: wrap;
    }

    .contact-info {
        width: 100%;
        background: var(--bg-cta-card);
        border-radius: var(--radius-primary);
        padding: 2rem;
        box-shadow: var(--shadow-smooth-strong);
        border: 1px solid var(--color-border);
        font-size: var(--text-lg);
        color: var(--text-highcontrast);
        display: flex;
        flex-direction: column;
    }

    .info-items {
        display: flex;
        flex-direction: column;
        gap: 1.5rem;
    }

    .info-item {
        display: flex;
        flex-direction: column;
        gap: 0.25rem;
    }

    a {
        color: var(--text-highcontrast);
        font-weight: normal;
        width: fit-content;
        font-family:
            "Manrope",
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

    a:hover,
    a:active {
        background-color: var(--color-primary-hover);
        color: white;
    }

    .puh-reverse {
        unicode-bidi: bidi-override;
        direction: rtl;
    }

    .label {
        font-size: var(--text-smaller);
        font-weight: 500;
        color: var(--text-subtle);
    }

    .contact-image {
        width: 100%;
        border-radius: var(--radius-primary);
        overflow: hidden;
        position: relative;
        box-shadow: var(--shadow-smooth-strong);
    }

    .contact-image img {
        width: 100%;
        object-fit: cover;
    }

    @media (min-width: 768px) {
        h1 {
            font-size: 2.75rem;
            margin-top: 0;
        }

        .contact-content {
            gap: 1.5rem;
        }
    }

    @media (min-width: 1024px) {
        .contact-info {
            width: 45%;
            padding: 3rem;
            font-size: var(--text-xl);
        }
        .contact-image {
            width: 40%;
        }
    }
</style>
