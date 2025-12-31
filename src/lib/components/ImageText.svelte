<script>
    let {
        imageSrc = "/images/placeholder.jpg",
        imageAlt = "Feature image",
        title = "Löydä myyntimahdollisuudet aikaisemmin",
        description = "Kokousvahti seuraa julkisen sektorin päätöksentekoa reaaliajassa ja tunnistaa relevantit myyntimahdollisuudet ennen kuin kilpailijasi. Saat tiedon päätöksistä, hankkeista ja tarpeista heti kun ne julkaistaan.",
        buttonText = "Lue lisää",
        buttonHref = "https://calendar.app.google/KB5ZkR7cQvuc31pt8",
        reverse = false,
    } = $props();
</script>

<section class="image-text-section">
    <div class="container">
        <div class="content-wrapper" class:reverse>
            <!-- Image -->
            <div class="image-container">
                <img src={imageSrc} alt={imageAlt} class="feature-image" />
            </div>

            <!-- Text Content -->
            <div class="text-content">
                <h2 class="section-title">{title}</h2>
                <p class="section-description">{description}</p>
                <a href={buttonHref} class="cta-button">
                    {buttonText}
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
                        <line x1="5" y1="12" x2="19" y2="12"></line>
                        <polyline points="12 5 19 12 12 19"></polyline>
                    </svg>
                </a>
            </div>
        </div>
    </div>
</section>

<style>
    .image-text-section {
        width: 100%;
        background-color: var(--bg-primary);
        padding: 4rem 0;
    }

    .container {
        max-width: var(--container-xl);
        margin: 0 auto;
        padding: 0 1rem;
    }

    .content-wrapper {
        display: flex;
        flex-direction: column;
        gap: 3rem;
        align-items: center;
    }

    .image-container {
        width: 100%;
        position: relative;
        overflow: hidden;
        border-radius: 10px;
        display: flex;
        justify-content: center;
        max-height: 400px;
        background-color: var(--color-surface);
    }

    .feature-image {
        height: 100%;
        width: auto;
        object-fit: contain;
    }

    .text-content {
        width: 100%;
        display: flex;
        flex-direction: column;
        gap: 1.5rem;
    }

    .section-title {
        color: var(--text-highcontrast);
        font-size: var(--headings-mobile);
        font-weight: 600;
        line-height: var(--leading-tight);
        margin: 0;
    }

    .section-description {
        font-size: var(--text-lg);
        line-height: var(--leading-relaxed);
        color: var(--text-subtle);
        margin: 0;
    }

    .cta-button {
        width: fit-content;
        display: inline-flex;
        align-items: center;
        justify-content: center;
        gap: 0.5rem;
        padding: var(--button-padding);
        font-weight: 600;
        font-size: var(--text-base);
        border-radius: 9999px;
        cursor: pointer;
        background: var(--button-bg);
        color: white;
        transition: var(--transition-fast);
        box-shadow: var(--shadow-md);
    }

    .cta-button:hover {
        background: var(--button-bg-hover);
    }

    .cta-button svg {
        transition: transform var(--transition-base);
    }

    .cta-button:hover svg {
        transform: translateX(4px);
    }

    /* Desktop layout */
    @media (min-width: 768px) {
        .content-wrapper {
            flex-direction: row;
            align-items: center;
            gap: 4rem;
        }

        .content-wrapper.reverse {
            flex-direction: row-reverse;
        }

        .image-container {
            flex: 1;
            min-width: 0;
        }

        .text-content {
            flex: 1;
            min-width: 0;
        }
    }

    /* Large desktop */
    @media (min-width: 1024px) {
        .section-title {
            font-size: var(--headings-tablet);
        }

        .image-container {
            aspect-ratio: 4/3;
        }

        .feature-image {
            height: 100%;
            object-fit: cover;
        }
    }
</style>
