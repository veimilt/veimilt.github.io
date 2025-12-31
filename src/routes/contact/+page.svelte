<script>
  import Contact from "$lib/components/Contact.svelte";
</script>

<svelte:head>
  <title>Yhteystiedot</title>
  <meta
    name="description"
    content="Ota meihin yhteyttä"
  />
  <link rel="preload" as="image" href="/images/kokousvahti.webp" fetchpriority="high">
</svelte:head>

<Contact
  data={{
    email: "contact@kokousvahti.fi",
    address: "Töölönkatu 35, 00100 Helsinki",
    ytunnus: "3343221-3",
    image: "/images/lauta.webp",
  }}
/>
