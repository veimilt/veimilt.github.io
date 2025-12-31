<script>
  let theme = $state("dark");
  let servicesDropdownOpen = $state(false);
  let mobileDialog;
  let mobileDropdownOpen = $state(false);

  function toggleTheme() {
    const newTheme = theme === "light" ? "dark" : "light";
    theme = newTheme;
    document.documentElement.setAttribute("data-theme", newTheme);
  }

  function toggleServicesDropdown() {
    servicesDropdownOpen = !servicesDropdownOpen;
    mobileDropdownOpen = !mobileDropdownOpen;
  }

  function closeServicesDropdown() {
    servicesDropdownOpen = false;
    mobileDropdownOpen = false;
  }

  function toggleMobileMenu() {
    if (mobileDialog) {
      if (mobileDialog.open) {
        mobileDialog.close();
      } else {
        mobileDialog.showModal();
      }
    }
  }

  function closeMobileMenu() {
    if (mobileDialog && mobileDialog.open) {
      mobileDropdownOpen = false;
      mobileDialog.close();
    }
  }

  const services = [
    {
      title: "Terveydenhuollon ja hoiva-alan toimijat",
      href: "/terveydenhuolto",
      icon: "health",
    },
    {
      title: "Rakennusalan toimijat",
      href: "/rakennusala",
      icon: "construction",
    },
    // {
    //   title: "Sosiaalipalveluiden kehitys",
    //   href: "/sosiaalipalvelut",
    //   icon: "social",
    // },
    // {
    //   title: "Koulutuspalveluiden kehitys",
    //   href: "/koulutus",
    //   icon: "education",
    // },
    // {
    //   title: "Kulttuuriprojektien seuranta",
    //   href: "/kulttuuri",
    //   icon: "culture",
    // },
  ];
</script>

<header>
  <div class="container">
    <div class="header-content">
      <a href="/" class="logo">
        <img
          class="logoimage"
          src="/images/kokousvahti_logo.webp"
          alt="kokousvahti logo"
        />
      </a>

      <div class="header-actions">
        <button
          class="theme-toggle"
          onclick={toggleTheme}
          aria-label="Toggle dark mode"
          title={theme === "light"
            ? "Vaihda tummaan tilaan"
            : "Vaihda vaaleaan tilaan"}
        >
          {#if theme === "light"}
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
              <path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"></path>
            </svg>
          {:else}
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
              <circle cx="12" cy="12" r="5"></circle>
              <line x1="12" y1="1" x2="12" y2="3"></line>
              <line x1="12" y1="21" x2="12" y2="23"></line>
              <line x1="4.22" y1="4.22" x2="5.64" y2="5.64"></line>
              <line x1="18.36" y1="18.36" x2="19.78" y2="19.78"></line>
              <line x1="1" y1="12" x2="3" y2="12"></line>
              <line x1="21" y1="12" x2="23" y2="12"></line>
              <line x1="4.22" y1="19.78" x2="5.64" y2="18.36"></line>
              <line x1="18.36" y1="5.64" x2="19.78" y2="4.22"></line>
            </svg>
          {/if}
        </button>

        <button
          class="mobile-toggle"
          onclick={toggleMobileMenu}
          aria-label="Toggle menu"
        >
          <span></span>
          <span></span>
          <span></span>
        </button>
      </div>

      <nav class="desktop-nav">
        <a class="navlink" href="/">Etusivu</a>
        <a class="navlink" href="/contact">Yhteydenotto</a>
        <div class="dropdown-wrapper">
          <button
            onclick={toggleServicesDropdown}
            class="dropdown-trigger"
            onmouseenter={() => (servicesDropdownOpen = true)}
          >
            Palvelumme
            <svg
              class="chevron"
              class:open={servicesDropdownOpen}
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
              <polyline points="6 9 12 15 18 9"></polyline>
            </svg>
          </button>

          {#if servicesDropdownOpen}
            <div
              class="dropdown-menu"
              onmouseenter={() => (servicesDropdownOpen = true)}
              onmouseleave={closeServicesDropdown}
            >
              <div class="dropdown-content">
                {#each services as service}
                  <a
                    class="dropdown-item"
                    href={service.href}
                    onclick={closeServicesDropdown}
                  >
                    <div class="item-icon">
                      {#if service.icon === "health"}
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="20"
                          height="20"
                          viewBox="0 0 24 24"
                          fill="none"
                          stroke="currentColor"
                          stroke-width="2.3"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        >
                          <path
                            d="M22 12h-2.48a2 2 0 0 0-1.93 1.46l-2.35 8.36a.25.25 0 0 1-.48 0L9.24 2.18a.25.25 0 0 0-.48 0l-2.35 8.36A2 2 0 0 1 4.49 12H2"
                          ></path>
                        </svg>
                      {:else if service.icon === "construction"}
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="20"
                          height="20"
                          viewBox="0 0 24 24"
                          fill="none"
                          stroke="currentColor"
                          stroke-width="2.3"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        >
                          <path
                            d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"
                          ></path>
                          <circle cx="12" cy="12" r="4"></circle>
                        </svg>
                      {:else if service.icon === "social"}
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="20"
                          height="20"
                          viewBox="0 0 24 24"
                          fill="none"
                          stroke="currentColor"
                          stroke-width="2.3"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        >
                          <path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2"
                          ></path>
                          <path d="M16 3.128a4 4 0 0 1 0 7.744"></path>
                          <path d="M22 21v-2a4 4 0 0 0-3-3.87"></path>
                          <circle cx="9" cy="7" r="4"></circle>
                        </svg>
                      {:else if service.icon === "education"}
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="20"
                          height="20"
                          viewBox="0 0 24 24"
                          fill="none"
                          stroke="currentColor"
                          stroke-width="2.3"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        >
                          <path d="M11 22H5.5a1 1 0 0 1 0-5h4.501"></path>
                          <path d="m21 22-1.879-1.878"></path>
                          <path
                            d="M3 19.5v-15A2.5 2.5 0 0 1 5.5 2H18a1 1 0 0 1 1 1v8"
                          ></path>
                          <circle cx="17" cy="18" r="3"></circle>
                        </svg>
                      {:else if service.icon === "culture"}
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          width="20"
                          height="20"
                          viewBox="0 0 24 24"
                          fill="none"
                          stroke="currentColor"
                          stroke-width="2.3"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                        >
                          <path d="M10 18v-7"></path>
                          <path
                            d="M11.12 2.198a2 2 0 0 1 1.76.006l7.866 3.847c.476.233.31.949-.22.949H3.474c-.53 0-.695-.716-.22-.949z"
                          ></path>
                          <path d="M14 18v-7"></path>
                          <path d="M18 18v-7"></path>
                          <path d="M3 22h18"></path>
                          <path d="M6 18v-7"></path>
                        </svg>
                      {/if}
                    </div>
                    <div class="item-content">
                      <div class="item-title">
                        {service.title}
                      </div>
                    </div>
                  </a>
                {/each}
              </div>
            </div>
          {/if}
        </div>
        <a
          class="navlink cta-button"
          href="https://calendar.app.google/KB5ZkR7cQvuc31pt8">Aloita nyt</a
        >
      </nav>
    </div>
  </div>
</header>

<dialog bind:this={mobileDialog} closedby="any">
  <button class="navlink closebtn" onclick={closeMobileMenu}>&#x2715;</button>
  <nav class="mobile-nav">
    <a class="mobile-navlink" href="/" onclick={closeMobileMenu}>Etusivu</a>

    <div class="mobile-dropdown-wrapper">
      <button class="mobile-dropdown-trigger" onclick={toggleServicesDropdown}>
        Palvelumme
        <svg
          class="chevron"
          class:open={servicesDropdownOpen}
          xmlns="http://www.w3.org/2000/svg"
          width="20"
          height="20"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2.3"
          stroke-linecap="round"
          stroke-linejoin="round"
        >
          <polyline points="6 9 12 15 18 9"></polyline>
        </svg>
      </button>

      <div
        class="mobile-dropdown-menu"
        class:open={mobileDropdownOpen}
        onclick={() => toggleServicesDropdown}
      >
        {#each services as service}
          <a
            class="mobile-dropdown-item"
            href={service.href}
            onclick={closeMobileMenu}
          >
            <div class="item-icon">
              {#if service.icon === "health"}
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="20"
                  height="20"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2.3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <path
                    d="M22 12h-2.48a2 2 0 0 0-1.93 1.46l-2.35 8.36a.25.25 0 0 1-.48 0L9.24 2.18a.25.25 0 0 0-.48 0l-2.35 8.36A2 2 0 0 1 4.49 12H2"
                  ></path>
                </svg>
              {:else if service.icon === "construction"}
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="20"
                  height="20"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2.3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <path
                    d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"
                  ></path>
                  <circle cx="12" cy="12" r="4"></circle>
                </svg>
              {:else if service.icon === "social"}
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="20"
                  height="20"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2.3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2"></path>
                  <path d="M16 3.128a4 4 0 0 1 0 7.744"></path>
                  <path d="M22 21v-2a4 4 0 0 0-3-3.87"></path>
                  <circle cx="9" cy="7" r="4"></circle>
                </svg>
              {:else if service.icon === "education"}
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="20"
                  height="20"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2.3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <path d="M11 22H5.5a1 1 0 0 1 0-5h4.501"></path>
                  <path d="m21 22-1.879-1.878"></path>
                  <path d="M3 19.5v-15A2.5 2.5 0 0 1 5.5 2H18a1 1 0 0 1 1 1v8"
                  ></path>
                  <circle cx="17" cy="18" r="3"></circle>
                </svg>
              {:else if service.icon === "culture"}
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="20"
                  height="20"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2.3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <path d="M10 18v-7"></path>
                  <path
                    d="M11.12 2.198a2 2 0 0 1 1.76.006l7.866 3.847c.476.233.31.949-.22.949H3.474c-.53 0-.695-.716-.22-.949z"
                  ></path>
                  <path d="M14 18v-7"></path>
                  <path d="M18 18v-7"></path>
                  <path d="M3 22h18"></path>
                  <path d="M6 18v-7"></path>
                </svg>
              {/if}
            </div>
            <div class="item-content">
              <div class="item-title">{service.title}</div>
            </div>
          </a>
        {/each}
      </div>
    </div>

    <a class="mobile-navlink" href="/contact" onclick={closeMobileMenu}
      >Yhteydenotto</a
    >
    <a
      class="mobile-navlink mobile-cta"
      href="https://calendar.app.google/KB5ZkR7cQvuc31pt8"
      onclick={closeMobileMenu}>Aloita nyt</a
    >
  </nav>
</dialog>

<style>
  header {
    border-bottom: 1px solid var(--header-border);
    position: sticky;
    top: 0;
    z-index: 1020;
    box-shadow: 0 0 1rem rgba(0, 0, 0, 0.075);
    background-color: var(--bg-header);
    backdrop-filter: blur(50px);
  }

  .container {
    max-width: var(--container-xl);
    margin: 0 auto;
    padding: 0 1rem;
  }

  .header-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 70px;
  }

  .logo {
    user-select: none;
  }

  .logoimage {
    width: 10rem;
  }

  .header-actions {
    display: flex;
    align-items: center;
    gap: 0.75rem;
  }

  .theme-toggle,
  .mobile-toggle {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 5px;
    width: 40px;
    height: 40px;
    border-radius: 10px;
    /* background-color: var(--bg-primary-subtle); */
    color: var(--text-highcontrast);
    /* border: 1px solid var(--color-border); */
    /* box-shadow: var(--shadow-sm); */
  }

  .theme-toggle:hover {
    background-color: var(--bg-primary-subtle);
  }

  .theme-toggle svg {
    transition: transform var(--transition-base);
  }

  .theme-toggle:hover svg {
    transform: rotate(20deg);
  }

  .mobile-toggle span {
    display: block;
    width: 20px;
    height: 2px;
    background-color: var(--text-highcontrast);
  }

  .desktop-nav {
    display: none;
    gap: 0.5rem;
    align-items: center;
  }

  .navlink,
  .dropdown-trigger {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 48px;
    padding: 0 1.5rem;
    border-radius: var(--radius-primary);
    color: var(--text-highcontrast);
    gap: 0.5rem;
    font-weight: 500;
    text-decoration: none;
    background: none;
    border: none;
    cursor: pointer;
    font-size: var(--text-base);
    transition: all var(--transition-fast);
    letter-spacing: 0.02em;
  }

  .navlink:hover,
  .dropdown-trigger:hover {
    background-color: var(--bg-primary-subtle);
  }

  .chevron {
    transition: transform var(--transition-base);
  }

  .chevron.open {
    transform: rotate(180deg);
  }

  .closebtn {
    position: absolute;
    top: 1.25rem;
    right: 1rem;
    /* background-color: var(--bg-primary-subtle); */
    border-radius: 10px;
    font-size: 1.5rem;
    padding: 1rem;
  }

  .dropdown-wrapper {
    position: relative;
  }

  .dropdown-menu {
    position: absolute;
    top: calc(100% + 0.5rem);
    left: 50%;
    transform: translateX(-50%);
    min-width: 400px;
    background-color: var(--bg-dialog);
    border: 1px solid var(--color-border);
    border-radius: var(--radius-primary);
    box-shadow: var(--shadow-xl);
    padding: 1rem;
    animation: fadeIn var(--transition-base);
    z-index: 1030;
  }

  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateX(-50%) translateY(-8px);
    }
    to {
      opacity: 1;
      transform: translateX(-50%) translateY(0);
    }
  }

  .dropdown-content {
    display: flex;
    flex-direction: column;
    gap: 0.25rem;
  }

  .dropdown-item {
    display: flex;
    align-items: center;
    gap: 0.75rem;
    padding: 0.75rem;
    border-radius: 1rem;
    transition: all var(--transition-fast);
    text-decoration: none;
    color: var(--text-highcontrast);
  }

  .dropdown-item:hover {
    background-color: var(--bg-primary-subtle);
  }

  .item-icon {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 36px;
    height: 36px;
    border-radius: var(--radius-full);
    background-color: var(--color-surface);
    color: var(--icon-primary);
    flex-shrink: 0;
    box-shadow: var(--shadow-sm);
  }

  .item-content {
    display: flex;
    flex-direction: column;
    flex: 1;
  }

  .item-title {
    font-weight: 500;
    line-height: 1.4;
  }

  .cta-button {
    background: var(--button-bg);
    color: white;
    font-weight: 600;
    height: auto;
    padding: 0.5rem 1.5rem !important;
    transition: background-color var(--transition-fast);
    box-shadow: var(--shadow-md);
    border-radius: var(--radius-full);
  }

  .cta-button:hover {
    background: var(--button-bg-hover);
  }

  dialog {
    position: fixed;
    top: 1.5rem;
    left: 1rem;
    right: 1rem;
    bottom: 1rem;
    width: calc(100% - 2rem);
    max-width: 500px;
    max-height: calc(100vh - 2rem);
    margin: 0 auto;
    padding: 0;
    border-radius: var(--radius-primary);
    background-color: var(--bg-dialog);
    box-shadow: var(--shadow-xl);
    border: 1px solid var(--color-border-dialog);
  }

  dialog::backdrop {
    backdrop-filter: blur(4px);
  }

  .mobile-nav {
    display: flex;
    flex-direction: column;
    padding: 1rem;
    gap: 0.5rem;
  }

  .mobile-navlink,
  .mobile-dropdown-trigger {
    display: flex;
    align-items: center;
    height: 60px;
    padding: 0 1rem;
    color: var(--text-highcontrast);
    text-decoration: none;
    font-weight: 500;
    font-size: var(--text-lg);
    border-radius: var(--radius-full);
    transition: all var(--transition-fast);
    gap: 1rem;
    letter-spacing: 0.02em;
  }

  .mobile-dropdown-wrapper {
    display: flex;
    flex-direction: column;
  }

  .mobile-dropdown-trigger {
    width: 100%;
    background: none;
    border: none;
    cursor: pointer;
  }

  .mobile-dropdown-menu {
    display: none;
    flex-direction: column;
    padding-left: 0.75rem;
    padding-top: 0.25rem;
  }

  .mobile-dropdown-menu.open {
    display: flex;
  }

  .mobile-dropdown-item {
    display: flex;
    align-items: center;
    gap: 0.75rem;
    min-height: 72px;
    padding: 0.75rem 0.5rem;
    color: var(--text-highcontrast);
    text-decoration: none;
    border-radius: 1rem;
    transition: all var(--transition-fast);
    font-size: var(--text-base);
  }

  .mobile-cta {
    background: var(--button-bg);
    color: white !important;
    padding: var(--button-padding);
    font-weight: 600;
    justify-content: center;
    margin-top: 0.5rem;
    border-radius: var(--radius-full);
  }

  .mobile-cta:hover {
    background: var(--button-bg-hover);
  }

  @media (min-width: 1024px) {
    .logoimage {
      width: 11.5rem;
    }

    .mobile-toggle {
      display: none !important;
    }

    dialog {
      display: none;
    }

    .header-actions {
      order: 2;
    }

    .desktop-nav {
      display: flex;
      order: 1;
      margin-left: auto;
      margin-right: 1rem;
    }
  }
</style>
