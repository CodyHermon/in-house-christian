<script lang="ts">
	import "../app.css";
	import Header from "$lib/components/ui/Header/Header.svelte";
	import Footer from "$lib/components/ui/Footer/Footer.svelte";

	let { children } = $props();
</script>

<Header />
<main>
	{@render children()}
</main>
<Footer />
