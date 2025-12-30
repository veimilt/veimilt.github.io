<script>
  import SubpageContent from "$lib/components/SubpageContent.svelte";
  import ImageText from "$lib/components/ImageText.svelte";

  const chapters = [
    {
      heading: "Kokousvahti rakennus- ja infrastruktuuri-alan tukena",
      content: `
				<p>Kokousvahti seuraa systemaattisesti kuntien ja kaupunkien rakennushankkeiden, infrastruktuuriprojektien ja kaavoituspäätösten valmistelua kokouspöytäkirjoista.</p>
				<p>Tekoäly tunnistaa automaattisesti sinulle relevantit hankkeet jo suunnitteluvaiheessa - kauan ennen virallisia hankintailmoituksia.</p>
			`,
    },
    {
      heading: "Seuraa investointeja ja hankkeita varhaisessa vaiheessa",
      content: `
				<p>Kokousvahti tunnistaa päätöksenteon eri vaiheissa:</p>
				<ul>
					<li><strong>Investointisuunnitelmat:</strong> Näet kunnan tai kaupungin pitkän tähtäimen rakennussuunnitelmat ja budjettiin varatut määrärahat</li>
					<li><strong>Kaavoituspäätökset:</strong> Seuraa asemakaavojen, yleiskaavojen ja kaavamuutosten valmistelua ja hyväksymistä</li>
					<li><strong>Rakennushankkeet:</strong> Tunnista koulujen, päiväkotien, liikuntahallien ja muiden julkisten rakennusten uudisrakennus- ja saneerausprojektit</li>
					<li><strong>Infrastruktuuri:</strong> Seuraa teiden, katujen, vesi- ja viemäriverkostojen sekä energiainfrastruktuurin kehittämishankkeita</li>
					<li><strong>Kiinteistöstrategia:</strong> Huomaa kunnan kiinteistöomaisuuden myynnit, ostot ja kehittämispäätökset</li>
				</ul>
			`,
    },
    {
      heading: "Hyödyt eri toimijoille",
      content: `
				<p><strong>Rakennusliikkeille:</strong> Näet jo suunnitteluvaiheessa tulevat uudisrakennuskohteet, laajennukset ja saneeraushankkeet. Voit valmistautua tarjouskilpailuihin ja rakentaa suhteita päättäjiin jo ennen virallisia hankintailmoituksia.</p>
				<p><strong>Suunnittelutoimistoille:</strong> Saat tiedon kaavoitushankkeista, rakennussuunnittelun tarpeista ja konsultointiprojekteista varhain. Voit tarjota asiantuntemustasi jo hankkeen alkuvaiheessa.</p>
				<p><strong>Infrayrityksille:</strong> Pysyt kartalla teiden, siltojen, tunneleiden ja verkostojen rakentamis- ja kunnossapitohankkeista. Näet, milloin kunta suunnittelee suurempia infrainvestointeja.</p>
				<p><strong>Materiaalitoimittajille:</strong> Kun tiedät tulevat hankkeet etukäteen, voit varautua kysyntään ja tarjota ratkaisujasi oikeaan aikaan.</p>
			`,
    },
    {
      heading: "Strateginen etu päätöksenteon seurannassa",
      content: `
				<p>Rakennus- ja infrahankkeissa päätöksenteko on pitkä prosessi. Strategiset linjaukset ja investointisuunnitelmat näkyvät kokouspöytäkirjoissa jopa vuosia ennen varsinaista rakentamisen aloitusta.</p>
				<p>Kokousvahdin avulla:</p>
				<ul>
					<li>Tunnistat hankkeet 1-3 vuotta ennen niiden toteutusta</li>
					<li>Voit vaikuttaa hankkeen sisältöön ja suunnitteluun jo varhaisessa vaiheessa</li>
					<li>Rakennat suhteita päättäjiin ja osoitat ymmärrystä kunnan tarpeista</li>
					<li>Vältät turhia tarjouksia - keskityt hankkeisiin, jotka todella toteutuvat</li>
					<li>Saat kilpailuetua muihin nähden, kun olet ensimmäisten joukossa tietoinen hankkeesta</li>
				</ul>
			`,
    },
    {
      heading: "Alueellinen seuranta",
      content: `
				<p>Määrittele itse, mitä alueita ja kuntia haluat seurata. Kokousvahti käy läpi valitsemiesi kuntien kokouspöytäkirjat ja ilmoittaa sinulle automaattisesti, kun sinua kiinnostavaa sisältöä ilmenee.</p>
				<p>Voit keskittyä esimerkiksi:</p>
				<ul>
					<li>Oman maakuntasi tai lähialueen kuntiin</li>
					<li>Kasvukeskuksiin ja kaupunkiseutuihin</li>
					<li>Tiettyihin erikoiskohteisiin (esim. koulut, sairaalat, liikuntapaikat)</li>
					<li>Tietyn kokoluokan investointeihin</li>
				</ul>
			`,
    },
  ];
</script>

<svelte:head>
  <title>Palvelut rakennusalalle</title>
  <meta
    name="description"
    content="Lue kuinka Kokousvahti auttaa rakennus- ja infrastruktuurialan päätöksenteossa"
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
            d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"
          ></path>
          <circle cx="12" cy="12" r="4"></circle>
        </svg>
      </div>
      <h1 class="hero-title">
        Kokousvahti rakennus- ja infrastruktuurialan päätöksenteon tukena
      </h1>
      <p class="hero-description">
        Kokousvahti auttaa sinua varautumaan kilpailutuksiin sekä uusiin
        säännöksiin
      </p>
    </div>
  </div>
</section>

<SubpageContent {chapters} />

<ImageText
  imageSrc="/images/lauta.webp"
  imageAlt="Dashboard preview"
  title="Palvelut Rakennus & infrastruktuurialan hankkeisiin ja toimijoille "
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
    padding-top: 0.25rem;
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
