<script>
  import SubpageContent from "$lib/components/SubpageContent.svelte";
  import ImageText from "$lib/components/ImageText.svelte";

  const chapters = [
    {
      heading: "Miksi kokousvahti?",
      content: `
				<p>Kokousvahti on tekoälyä hyödyntävä palvelu, joka analysoi julkisen sektorin kokouspöytäkirjat ja tunnistaa terveydenhuollon ja hoiva-alan kehitystarpeita sekä päätöksiä reaaliajassa.</p>
				<p>Palvelumme auttaa palveluntarjoajia, teknologiayrityksiä ja konsultteja pysymään ajan tasalla kuntien ja sairaanhoitopiirien strategisista linjauksista ja investointipäätöksistä.</p>
			`,
    },
    {
      heading: "Miten Kokousvahti tukee palveluiden kehittämistä?",
      content: `
				<p>Kokousvahti seuraa systemaattisesti terveydenhuollon ja hoiva-alan päätöksentekoa:</p>
				<ul>
					<li><strong>Strategiset linjaukset:</strong> Tunnistamme kuntien ja sairaanhoitopiirien pitkän aikavälin suunnitelmat ja painopistealueet</li>
					<li><strong>Investointipäätökset:</strong> Seuraamme tieto- ja hoitojärjestelmien uudistuksia, laitehankintoja ja tilainvestointeja</li>
					<li><strong>Palvelurakenteen muutokset:</strong> Huomaamme sote-uudistukseen liittyvät päätökset ja palveluverkkojen kehittämistarpeet</li>
					<li><strong>Digitalisaatiohankkeet:</strong> Tunnistamme etähoito-, tekoäly- ja tietojärjestelmäprojektit varhaisessa vaiheessa</li>
				</ul>
			`,
    },
    {
      heading: "Hyödyt päätöksenteon tukena",
      content: `
				<p><strong>Palveluntuottajille:</strong> Näet etukäteen, kun kunnat suunnittelevat kotihoidon, vanhustenhuollon tai erikoissairaanhoidon palveluhankintojen kilpailutuksia. Voit valmistautua tarjouspyyntöihin ja kehittää palveluitasi vastaamaan todellisia tarpeita.</p>
				<p><strong>Teknologiayrityksille:</strong> Saat tiedon digitalisaatiopäätöksistä, järjestelmäintegraatioista ja innovaatiokokeiluista ennen virallisia hankintailmoituksia. Voit tarjota ratkaisujasi oikeaan aikaan ja osoittaa ymmärrystä asiakkaan strategisista tavoitteista.</p>
				<p><strong>Konsulteille ja kehittäjille:</strong> Pysyt kartalla organisaatiomuutoksista, prosessikehityshankkeista ja koulutussuunnitelmista. Voit kohdentaa asiantuntemuksesi sinne, missä muutostarvetta on tunnistettu.</p>
			`,
    },
    {
      heading: "Miksi seuranta on tärkeää?",
      content: `
				<p>Terveydenhuollon ja hoiva-alan päätöksenteko on moniportaista ja hidasta. Strategiset linjaukset näkyvät kokouspöytäkirjoissa kuukausia tai jopa vuosia ennen varsinaisia hankintapäätöksiä.</p>
				<p>Kokousvahdin avulla:</p>
				<ul>
					<li>Olet askeleen edellä kilpailijoita tunnistamalla kehitystarpeet varhain</li>
					<li>Voit osallistua päätöksentekoon tarjoamalla asiantuntemustasi ennen lopullisia päätöksiä</li>
					<li>Ymmärrät paremmin asiakkaittesi todellisia haasteita ja strategisia tavoitteita</li>
					<li>Säästät aikaa ja resursseja kohdentamalla myyntityösi sinne, missä on todellista kysyntää</li>
				</ul>
			`,
    },
  ];
</script>

<svelte:head>
  <title>Palvelut terveydenhuollolle</title>
  <meta
    name="description"
    content="Lue kuinka Kokousvahti auttaa terveydenhuollon alan päätöksenteossa"
  />
  <link
    rel="preload"
    as="image"
    href="/bg/pisarat.webp"
    fetchpriority="high"
  />
</svelte:head>

<section class="hero-container">
  <div class="hero">
    <div class="blur-layer"></div>
    <div class="hero-content">
      <div class="hero-icon">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="2.5rem"
          height="2.5rem"
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
      </div>
      <h1 class="hero-title">
        Kokousvahdin hyödyt terveydenhuollossa ja hoiva-alalla
      </h1>
      <p class="hero-description">
        Kokousvahti auttaa sinua päätöksenteossa palveluiden kehittämisessä
      </p>
    </div>
  </div>
</section>

<SubpageContent subtitle="Palveluiden kehittäminen" {chapters} />
<ImageText
  imageSrc="/images/pink.webp"
  imageAlt="Dashboard preview"
  title="Palvelut terveydenhuollolle"
  description="Tekstiä miten terveydenhuolto ja sosiaaliala voi hyödyntää sekä tällä hetkellä hyödyntää kokousvahdin palveluita"
  buttonText="Aloita nyt"
/>

<style>
  .hero-container {
    width: 100%;
    /* padding: 0.75rem 0.5rem; */
    background-color: var(--bg-primary);
  }

  .hero {
    height: 100%;
    padding: 3rem 1.5rem;
    background-color: var(--bg-primary);
    background-image: url("/bg/pisarat.webp");
    background-size: cover;
    background-position: center;
    border-radius: 1rem;
    position: relative;
    overflow: hidden;
  }

  .blur-layer {
    position: absolute;
    inset: 0;
    content: "";
    backdrop-filter: blur(15px);
    z-index: 1;
  }

  .hero-content {
    width: 100%;
    max-width: var(--container-xl);
    margin: 0 auto;
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    position: relative;
    z-index: 100;
  }

  .hero-icon {
    width: 4rem;
    height: 4rem;
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgba(255, 255, 255, 0.875);
    border-radius: 9999px;
    padding: 1rem;
    box-shadow: var(--shadow-md);
    margin-bottom: 1rem;
  }

  .hero-icon svg {
    color: var(--color-primary);
  }

  .hero-title {
    font-size: 1.875rem;
    line-height: 1.1;
    color: var(--text-highcontrast-black);
    margin: 0;
    text-shadow: 0 0 1rem rgba(0, 0, 0, 0.1);
    margin-bottom: 1rem;
  }

  .hero-description {
    font-size: var(--text-lg);
    color: var(--text-highcontrast-black);
    margin: 0;
  }

  @media (min-width: 768px) {
    .hero {
      padding: 4rem 3rem;
    }

    .hero-title {
      font-size: var(--headings-tablet);
    }

    .hero-description {
      font-size: var(--text-xl);
    }

    .hero-icon {
      width: 4rem;
      height: 4rem;
    }
  }

  @media (min-width: 1024px) {
    .hero-title {
      font-size: var(--headings-laptop);
    }
  }
</style>
