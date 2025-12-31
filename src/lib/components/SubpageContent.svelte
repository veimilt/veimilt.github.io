<script>
    let { chapters = [] } = $props();
</script>

<!-- main container -->
<div class="subpage">
    {#each chapters as chapter, i}
        <!-- container blocks 100% width -->
        <article class="page-content">
            <!-- width capped content -->
            <div class="chapters">
                <section class="chapter" id="chapter-{i + 1}">
                    {#if chapter.heading}
                        <h2 class="chapter-heading">{chapter.heading}</h2>
                    {/if}

                    {#if chapter.content}
                        <div class="chapter-content">
                            <p>
                                {@html chapter.content}
                            </p>
                        </div>
                    {/if}
                </section>
            </div>
        </article>
    {/each}
</div>

<style>
    h1,
    h2,
    h3,
    h4,
    p {
        max-width: 1000px;
    }
    .subpage {
        background-color: var(--bg-primary);
        padding-top: 3rem;
        padding-bottom: 2rem;
    }
    .page-content {
        width: 100%;

        padding: 4rem 2rem;
        padding-top: 2rem;
    }

    .page-content:nth-child(1),
    .page-content:nth-child(2),
    .page-content:nth-child(5) {
        background: var(--card-bg-primary);
    }

    .chapters {
        display: flex;
        flex-direction: column;
        gap: 4rem;
        max-width: var(--container-xl);
        margin: 0 auto;
    }

    /* .page-content:nth-child(3) div,
    .page-content:nth-child(4) div,
    .page-content:nth-child(5) div {
        max-width: var(--container-lg);
        
    } */

    .chapter {
        display: flex;
        flex-direction: column;
        gap: 1rem;
        padding-top: 1rem;
    }

    .chapter-heading {
        font-size: var(--headings-mobile);
        font-weight: 700;
        line-height: 1.2;
        letter-spacing: -0.01em;
        color: var(--text-highcontrast);
        margin: 0;
        margin-bottom: 0.5rem;
    }

    .chapter-content {
        font-size: var(--text-base);
        line-height: var(--leading-relaxed);
        color: var(--text-subtle);
    }

    /* Typography for content */
    .chapter-content :global(p) {
        margin: 0 0 2rem 0;
    }

    .chapter-content :global(p:last-child) {
        margin-bottom: 0;
    }

    .chapter-content :global(strong) {
        font-weight: 600;
        color: var(--text-highcontrast);
    }

    .chapter-content :global(ul),
    .chapter-content :global(ol) {
        margin: 0 0 var(--spacing-lg, 2rem) 0;
        padding-left: 1.5rem;
    }

    .chapter-content :global(li) {
        margin-bottom: var(--spacing-sm, 0.5rem);
    }

    .chapter-content :global(li:last-child) {
        margin-bottom: 0;
    }

    @media (min-width: 768px) {
        .chapters {
            gap: 5rem;
        }

        .chapter {
            gap: 2rem;
        }
    }

    @media (min-width: 1024px) {
        .chapter-heading {
            font-size: var(--headings-tablet);
        }

        .page-content:nth-child(3),
        .page-content:nth-child(4),
        .page-content:nth-child(5) {
            padding: 4rem;
            padding-top: 3rem;
        }

        .chapter{
            padding-top: 2rem;
        }
    }
</style>
