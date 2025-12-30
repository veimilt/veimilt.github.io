<script>
  const steps = [
    {
      number: 1,
      icon: "search",
      title: "Määritetään yhdessä haku",
      description:
        "Katsotaan yhdessä meidän tuntemien parhaiden käytäntöjen kautta mitä etsimme dokumenteista.",
    },
    {
      number: 2,
      icon: "email",
      title: "Saat ensimmäiset raportit sähköpostiisi",
      description:
        "Pian aloituspalaverin jälkeen pääset jo käsiksi ensimmäiseen raporttiin",
    },
    {
      number: 3,
      icon: "iterate",
      title: "Jatkuva iteraatio",
      description:
        "Palautteesi perusteella pystymme jatkuvasti iteroimaan tuloksia osuvimmiksi",
    },
  ];

  const insights = [
    {
      city: "Helsinki",
      signals: [
        {
          text: "On budjetoinut 2 miljoonaa euroa tekoälykehitykseen",
          status: "high",
          action: "Ymmärrä",
        },
        {
          text: "Valmistelee suuren rakennushankkeen kilpailutusta",
          status: "medium",
          action: "Vaikuta",
        },
        {
          text: "Valmistelee uuden vanhusten asumisyksikön avaamista",
          status: "ready",
          action: "Voita",
        },
      ],
    },
  ];

  const actionCategories = [
    {
      title: "Ymmärrä",
      color: "rgba(150, 204, 255, 0.25)",
      description:
        "Mitä toimija priorisoi, mitkä tulevat hankkeet ja tarpeet koskevat sinua",
    },
    {
      title: "Vaikuta",

      color: "rgba(79, 170, 255, 0.25)",
      description:
        "Tapaa, keskustele, soita, viestittele ja vaikuta tarpeeseen / hankkeeseen liittyen",
    },
    {
      title: "Voita",
      color: "rgba(0, 206, 209, 0.25)",
      description: "Olet etulyöntiasemassa kilpailutuksen tullessa ulos",
    },
  ];
</script>

<section class="usage">
  <div class="container">
    <div class="usage-header">
      <h2 class="usage-title">Käyttöönotto on helppoa ja nopeaa</h2>
      <p class="usage-description">
        Autamme sinua palvelun käyttöönotossa sekä haun määrittelyssä.
        Parannamme hakutuloksia jatkuvasti palautteesi perusteella. Neuvomme
        myös, mitä dokumentaatiosta kannattaa etsiä.
      </p>
    </div>

    <div class="content-grid">
      <!-- LEFT: Insights Chart -->
      <div class="insights-section">
        <h3 class="insights-title">Esimerkkejä signaaleista</h3>

        {#each insights as insight}
          <div class="insight-card">
            <div class="city-header">
              <h4 class="city-name">{insight.city}</h4>
            </div>

            <ul class="signals-list">
              {#each insight.signals as signal}
                <li class="signal-item" data-status={signal.status}>
                  <div class="signal-content">
                    <p class="signal-text">{signal.text}</p>
                  </div>
                </li>
              {/each}
            </ul>

            <div class="actions-legend">
              {#each actionCategories as category}
                <div class="action-category">
                  <div
                    class="action-info"
                    style="background-color: {category.color}"
                  >
                    <h5 class="action-title">{category.title}</h5>
                    <p class="action-description">{category.description}</p>
                  </div>
                </div>
              {/each}
            </div>
          </div>
        {/each}
      </div>

      <!-- RIGHT: Steps -->
      <div class="steps-section">
        <h3 class="kayttoonotto-title">Käyttöönoton vaiheet</h3>

        {#each steps as step, index}
          <div class="step-item">
            <div class="step-icon-wrapper">
              <div class="step-number">{step.number}</div>
              {#if step.icon === "search"}
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2.3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <circle cx="11" cy="11" r="8"></circle>
                  <path d="m21 21-4.35-4.35"></path>
                </svg>
              {:else if step.icon === "email"}
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
                    d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"
                  ></path>
                  <polyline points="22,6 12,13 2,6"></polyline>
                </svg>
              {:else if step.icon === "iterate"}
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2.3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <path
                    d="M21.5 2v6h-6M2.5 22v-6h6M2 11.5a10 10 0 0 1 18.8-4.3M22 12.5a10 10 0 0 1-18.8 4.2"
                  ></path>
                </svg>
              {/if}
            </div>
            <div class="step-content">
              <h3 class="step-title">{step.title}</h3>
              <p class="step-description">{step.description}</p>
            </div>
          </div>

          {#if index < steps.length - 1}
            <div class="step-arrow">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2.3"
                stroke-linecap="round"
                stroke-linejoin="round"
              >
                <line x1="12" y1="5" x2="12" y2="19"></line>
                <polyline points="19 12 12 19 5 12"></polyline>
              </svg>
            </div>
          {/if}
        {/each}

        <!-- <button class="cta-button">
          Aloita nyt
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2.5"
            stroke-linecap="round"
            stroke-linejoin="round"
          >
            <path d="M5 12h14"></path>
            <path d="m12 5 7 7-7 7"></path>
          </svg>
        </button> -->
      </div>
    </div>
  </div>
</section>

<style>

  .usage {
    width: 100%;
    padding: 2rem 0;
    background-color: var(--bg-primary);
  }

  .container {
    max-width: var(--container-xl);
    margin: 0 auto;
    padding: 0 1rem;
  }

  .usage-header {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    margin-bottom: 4rem;
    gap: 2rem;
  }

  .usage-title {
    font-size: var(--headings-mobile);
    font-weight: 600;
    line-height: var(--leading-tight);
    color: var(--text-highcontrast);
    max-width: 48rem;
    margin: 0;
  }

  .usage-description {
    font-size: var(--text-lg);
    line-height: var(--leading-relaxed);
    color: var(--text-subtle);
    max-width: 48rem;
    margin: 0;
  }

  .content-grid {
    display: grid;
    gap: 4rem;
    grid-template-columns: 1fr;
  }

  /* Insights Section */
  .insights-section {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  .insights-title,
  .kayttoonotto-title {
    font-size: var(--text-2xl);
    font-weight: 600;
    color: var(--text-highcontrast);
    margin: 0 0 0.5rem 0;
  }

  .kayttoonotto-title {
    margin: 0 0 1rem 0;
  }

  .insight-card {
    background: var(--card-bg-primary);
    border: 1px solid var(--color-border);
    border-radius: var(--radius-primary);
    padding: 1.5rem;
    color: var(--text-highcontrast);
    font-size: var(--text-normal);
    box-shadow: var(--shadow-smooth-strong);
  }

  .city-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 1.5rem;
  }

  .city-name {
    font-size: var(--text-xl);
    font-weight: 600;
    margin: 0;
    background-color: var(--color-primary-hover);
    color: white;
    padding: 0.5rem 0.75rem;
    border-radius: 9999px;
  }

  .signals-list {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    margin-bottom: 2rem;
    list-style-type: disc;
    padding-left: 1rem;
  }

  .signal-item {
    display: list-item;
    align-items: flex-start;
  }

  .signal-content {
    flex: 1;
  }

  .signal-text {
    margin: 0;
    line-height: var(--leading-relaxed);
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    font-weight: 600;

  }

  .actions-legend {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    padding-top: 1.5rem;
    border-top: 1px solid var(--color-border);
  }

  .action-category {
    display: flex;
    gap: 0.75rem;
    align-items: flex-start;
  }

  .action-info {
    flex: 1;
    padding: 1rem 1.25rem;
    border-radius: 10px;
    min-height: 100px;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .action-title {
    font-size: var(--text-xl);
    font-weight: 600;
    margin-bottom: 0.5rem;
  }

  .action-description {
    font-size: var(--text-smaller);
    margin: 0;
    line-height: var(--leading-relaxed);
  }

  /* Steps Section */
  .steps-section {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    height: 100%;
  }

  .step-item {
    display: flex;
    align-items: center;
    background: var(--card-bg-primary);
    border: 1px solid var(--color-border);
    border-radius: 3rem;
    padding: 1.5rem;
    gap: 1.5rem;
    flex-grow: 1;
    box-shadow: 2px 4px 1rem rgba(0, 0, 0, 0.075);
  }

  .step-icon-wrapper {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 64px;
    height: 64px;
    background-color: var(--bg-primary-subtle);
    color: var(--color-primary);
    border-radius: var(--radius-full);
    flex-shrink: 0;
  }

  .step-number {
    position: absolute;
    top: -8px;
    left: -8px;
    width: 24px;
    height: 24px;
    background-color: var(--color-primary);
    color: white;
    border-radius: var(--radius-full);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: var(--text-sm);
    font-weight: 600;
  }

  .step-content {
    flex: 1;
  }

  .step-title {
    font-size: var(--text-xl);
    font-weight: 600;
    color: var(--text-highcontrast);
    margin: 0 0 0.75rem 0;
  }

  .step-description {
    font-size: var(--text-normal);
    color: var(--text-subtle);
    margin: 0;
    line-height: var(--leading-relaxed);
  }

  .step-arrow {
    display: flex;
    justify-content: center;
    color: var(--color-primary);
    padding: 0.25rem 0;
  }

  /* .cta-button {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 0.5rem;
    width: 100%;
    padding: 0.75rem 2rem;
    background: var(--color-primary);
    color: white;
    font-weight: 600;
    font-size: var(--text-base);
    border-radius: var(--radius-md);
    text-decoration: none;
    box-shadow: var(--shadow-md);
    margin-top: 1.25rem;
  }

  .cta-button:hover {
    background-color: var(--color-primary-hover);
    color: white;
  }

  .cta-button svg {
    transition: transform var(--transition-base);
  }

  .cta-button:hover svg {
    transform: translateX(4px);
  } */

  /* Desktop */
  @media (min-width: 768px) {
    .usage {
      padding-top: 4rem;
    }

    .usage-title {
      font-size: var(--headings-tablet);
    }

    .content-grid {
      grid-template-columns: 1fr 1fr;
      align-items: start;
    }

    /* .cta-button {
      width: auto;
    } */
  }

  @media (min-width: 1024px) {
    .usage-header {
      gap: 1.5rem;
      margin-bottom: 5rem;
    }

    .usage-description {
      font-size: var(--text-xl);
    }

    .step-item {
      padding: 2rem;
    }
  }
</style>
