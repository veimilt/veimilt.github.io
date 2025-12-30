
<section class="logo-section">
    <div class="logo-container">
        <p class="logo-label">Palveluihimme luottavat</p>

        <div class="logo-grid">
            <div class="logo-wrapper">
                <img src="/images/esperi_logo.svg" alt="" />
            </div>

            <div class="logo-wrapper">
                <img src="/images/EQ_Logo.svg" alt="" />
            </div>

            <div class="logo-wrapper">
                <img src="images/sitowise.svg" alt="" />
            </div>

            <div class="logo-wrapper">
                <img src="/images/solum_logo.png" alt="" />
            </div>
        </div>
    </div>
</section>

<style>
    .logo-section {
        width: 100%;
        padding: 3rem 0 1rem 0;
        padding-bottom: 2rem;
        background-color: var(--bg-hero);
    }

    .logo-container {
        max-width: var(--container-lg);
        margin: 0 auto;
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 0 1rem;
        gap: 1rem;
    }

    .logo-label {
        font-size: var(--text-smaller);
        color: var(--text-subtle);
        text-transform: uppercase;
        letter-spacing: 0.03em;
        margin: 0;
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

    .logo-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 1rem;
        width: fit-content;
        align-items: center;
        justify-items: center;
        justify-items: center;
    }

    .logo-wrapper {
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        max-width: 200px;
        height: 100%;
        padding: 2rem;
        user-select: none;
        pointer-events: none;
    }
    .logo-wrapper:nth-child(2),
    .logo-wrapper:nth-child(3),
    .logo-wrapper:nth-child(4) {
        padding: 2rem 3rem;
    }

    .logo-wrapper:nth-child(4) {
        padding: 2rem 3rem;
        padding-bottom: 2.5rem;
    }

    .logo-wrapper img {
        filter: var(--logo-filter);
    }

    @media (min-width: 1024px) {
        .logo-label {
            font-size: var(--text-base);
        }

        .logo-section {
            padding: 5rem 0;
        }

        .logo-grid {
            grid-template-columns: repeat(4, 1fr);
            max-width: 1100px;
        }
    }
</style>
