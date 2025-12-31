<script>
  import { onMount } from "svelte";
  import { spring } from "svelte/motion";

  // Tighter spring settings to prevent oscillation
  const stat1 = spring(0, { stiffness: 0.1, damping: 0.8 });
  const stat2 = spring(0, { stiffness: 0.1, damping: 0.8 });
  const stat3 = spring(0, { stiffness: 0.1, damping: 0.8 });
  const stat2Change = spring(0, { stiffness: 0.1, damping: 0.8 });

  let isVisible = false;

  onMount(() => {
    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting && !isVisible) {
            isVisible = true;
            // Start animations with a slight delay
            setTimeout(() => {
              stat1.set(1000);
              stat2.set(1000);
              stat3.set(1000);
              stat2Change.set(50);
            }, 100);
          }
        });
      },
      { threshold: 0.2 },
    );

    const section = document.querySelector(".stats");
    if (section) observer.observe(section);

    return () => observer.disconnect();
  });

  // Format number with space separator and proper rounding
  function formatNumber(num) {
    const rounded = Math.round(num);
    return rounded.toLocaleString("fi-FI").replace(/,/g, "\u00A0");
  }
</script>

<section class="stats">
  <div class="container">
    <div class="stats-pill">
      <div class="stats-grid">
        <!-- KPI 1 -->
        <div class="stat-item">
          <p class="stat-number">{formatNumber($stat1)}+</p>
          <p class="stat-label">Julkiselta sektorilta luettuja dokumentteja</p>
        </div>

        <!-- KPI 2 -->
        <div class="stat-item">
          <p class="stat-number">{formatNumber($stat2)}+</p>
          <p class="stat-label">Luetut dokumentit YTD</p>
        </div>

        <!-- KPI 3 -->
        <div class="stat-item">
          <p class="stat-number">{formatNumber($stat3)}+</p>
          <p class="stat-label">Edelliset 30 päivää</p>
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  .stats {
    width: 100%;
    padding: 2.5rem 1rem;
    /* padding-bottom: 4rem; */
    background: var(--stat-bg);
  }

  .container {
    width: 100%;
    margin: 0 auto;
    /* background: var(--card-bg-primary); */
    padding: 2rem 3rem;
    padding-top: 0rem;
    /* box-shadow: 2px 4px 1rem rgba(0, 0, 0, 0.075);
    border-radius: var(--radius-primary);
    border: 1px solid var(--color-border);
    corner-shape: var(--corner-primary); */
  }

  .stats-pill {
    width: 100%;
    max-width: var(--container-lg);
    margin: 0 auto;
  }
  .stats-grid {
    display: grid;
    gap: 3rem;
    grid-template-columns: 1fr;
  }

  .stat-item {
    display: flex;
    flex-direction: column;
  }

  .stat-number {
    font-size: var(--headings-tablet);
    font-weight: bold;
    line-height: var(--leading-tight);
    color: var(--stat-color);
    margin: 0;
    font-variant-numeric: tabular-nums;
  }

  .stat-label {
    margin-top: 0.5rem;
    font-size: var(--text-lg);
    color: var(--stat-color);
    line-height: var(--leading-normal);
    margin-bottom: 0;
  }

  /* Tablet and up */
  @media (min-width: 640px) {
    .stats-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  /* Desktop */
  @media (min-width: 1024px) {
    /* .stats {
      background: linear-gradient(
        to bottom,
        var(--accent-bg-brown) 0%,
        var(--accent-bg-brown) 50%,
        var(--bg-blue-alternate) 50%,
        var(--bg-blue-alternate) 100%
      );
    } */

    .container {
      padding: 3rem 4rem;
      padding-top: 2rem;
    }

    .stats-grid {
      grid-template-columns: repeat(3, 1fr);
    }
    .stat-item {
      align-items: center;
      text-align: center;
    }

    .stat-number {
      font-size: 3rem;
    }
  }
  @media (min-width: 1236px) {
    .stats {
      padding: 4rem 1rem;
    }
  }
</style>
