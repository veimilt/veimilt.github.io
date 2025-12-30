<script>
	import favicon from "$lib/assets/favicon.ico";
	import "../app.css";
	let { children } = $props();
	import Header from "$lib/components/Header.svelte";
	import Footer from "$lib/components/Footer.svelte";
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<Header />

{@render children()}

<Footer />
