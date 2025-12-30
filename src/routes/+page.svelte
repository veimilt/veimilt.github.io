<script>
    import Hero from "$lib/components/Hero.svelte";
    import TrustedBy from "$lib/components/TrustedBy.svelte";
    import Features from "$lib/components/Features.svelte";
    import Stats from "$lib/components/Stats.svelte";
    import Integrations from "$lib/components/Integrations.svelte";
    import Usage from "$lib/components/Usage.svelte";
    import CTA from "$lib/components/CTA.svelte";
</script>

<svelte:head>
    <title>Kokousvahti • Etusivu</title>
    <meta
        name="description"
        content="Kokousvahti - Voita julkisen sektorin hankinnat ennen niiden julkaisua"
    />
</svelte:head>

<Hero />
<TrustedBy />
<Features />
<Stats />
<Integrations />
<Usage />
<CTA />
