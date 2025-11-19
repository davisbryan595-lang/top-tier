<script lang="ts">
	import '../app.css';

	let { children } = $props();
</script>

<svelte:head>
	<title>Top Tier Towing & Recovery | 24/7 Emergency Towing Independence MO</title>
	<meta name="description" content="24/7 Emergency towing services in Independence, Missouri. Fast, reliable roadside assistance. Call 816-805-9240 now!" />
	<meta name="viewport" content="width=device-width, initial-scale=1" />
	<meta name="theme-color" content="#9D00FF" />
	<meta property="og:title" content="Top Tier Towing & Recovery LLC" />
	<meta property="og:description" content="Faster Than Your Insurance Company - 24/7 Emergency Towing" />
	<meta property="og:image" content="https://hebbkx1anhila5yf.public.blob.vercel-storage.com/top2-EHYTkCqOssSZhr2aHXCRC5QAZSM7Ny.jpg" />
</svelte:head>

<div class="min-h-screen bg-black-carbon">
	{@render children()}
</div>

<style>
	:global(body) {
		margin: 0;
		padding: 0;
		font-family: 'Geist', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
		background: #0F0F0F;
	}

	:global(html) {
		scroll-behavior: smooth;
	}
</style>
