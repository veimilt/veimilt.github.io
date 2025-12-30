<script>
    const integrations = [
        {
            name: "Salesforce",
            description: "Saumaton integraatio CRM-järjestelmiin",
            logo: "/images/integrations_1.svg",
        },
        {
            name: "Microsoft Dynamics",
            description: "Synkronoi projektitiimit ja tehtävät",
            logo: "/images/integrations_3.svg",
        },
        {
            name: "HubSpot",
            description: "Yhdistä tiedot suoraan CRM:ääsi",
            logo: "/images/integrations_2.svg",
        },
    ];
</script>

<section class="integrations">
    <div class="container">
        <div class="integrations-header">
            <h2 class="integrations-title">
                Toimii saumattomasti olemassa olevien työkalujesi kanssa
            </h2>
            <p class="integrations-description">
                Kokousvahti integroituu helposti käyttämiisi järjestelmiin.
                Tiedot kulkevat automaattisesti sinne, missä niitä tarvitset.
            </p>
        </div>

        <div class="integrations-grid">
            {#each integrations as integration}
                <div class="integration-item">
                    <img
                        src={integration.logo}
                        alt={integration.name}
                        class="integration-logo"
                    />
                    <div class="integration-textbox">
                        <h3 class="integration-title">
                            {integration.name}
                        </h3>
                        <p class="integration-description">
                            {integration.description}
                        </p>
                    </div>
                </div>
            {/each}
        </div>
    </div>
</section>

<style>
    .integrations {
        width: 100%;
        padding: 4rem 0;
        padding-bottom: 0.5rem;
        /* background-image: linear-gradient(
            #f0f3f7
        ); */
        background: var(--bg-primary);
    }

    .container {
        max-width: var(--container-xl);
        margin: 0 auto;
        padding: 0 1rem;
    }

    .integrations-header {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        margin-bottom: 4rem;
        gap: 2rem;
    }

    .integrations-title {
        font-size: var(--headings-mobile);
        font-weight: 600;
        line-height: var(--leading-tight);
        color: var(--text-highcontrast);
        margin: 0;
    }

    .integrations-description {
        font-size: var(--text-lg);
        line-height: var(--leading-relaxed);
        color: var(--text-subtle);
        max-width: 42rem;
        margin: 0;
    }

    .integrations-grid {
        display: grid;
        gap: 1.5rem;
        grid-template-columns: 1fr;
        margin-bottom: 4rem;
    }

    .integration-item {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        background: var(--card-bg-primary);
        padding: 2rem;
        border-radius: var(--radius-primary);
        box-shadow: var(--shadow-smooth);
        border: 1px solid var(--color-border);
        min-height: 275px;
    }

    .integration-logo {
        width: 100px;
        height: 100px;
        max-height: 85px;
        max-width: 100px;
        object-fit: contain;
        margin-bottom: 1rem;
        user-select: none;
        pointer-events: none;
    }

    .integration-textbox {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        flex-grow: 1;
    }

    .integration-title {
        font-size: var(--text-xl);
        font-weight: 600;
        color: var(--text-highcontrast);
        margin: 0 0 0.5rem 0;
    }

    .integration-description {
        font-size: var(--text-base);
        line-height: var(--leading-relaxed);
        color: var(--text-subtle);
        margin: 0;
        max-width: 20rem;
        font-weight: normal;
        max-width: 300px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    /* .integrations-footer {
        display: flex;
        justify-content: center;
        padding-top: 2rem;
        border-top: 1px solid var(--color-border);
    } */

    /* .footer-text {
        font-size: var(--text-base);
        color: var(--color-text-light);
        margin: 0;
    } */

    /* Tablet */
    @media (min-width: 640px) {
        .integrations-grid {
            grid-template-columns: repeat(2, 1fr);
        }
    }

    /* Desktop */
    @media (min-width: 768px) {
        .integrations {
            padding-bottom: 2rem;
        }
        .integrations-title {
            font-size: var(--headings-tablet);
        }

        .integration-title {
            font-size: var(--text-2xl);
        }
    }

    @media (min-width: 1024px) {
        .integrations {
            padding-top: 7rem;
        }

        .integrations-header {
            gap: 1.5rem;
        }

        .integrations-description {
            font-size: var(--text-xl);
        }

        .integrations-grid {
            grid-template-columns: repeat(3, 1fr);
        }
    }
</style>
