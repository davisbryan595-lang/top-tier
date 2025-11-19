<script lang="ts">
	import Navbar from '../lib/components/navbar.svelte';
	import Hero from '../lib/components/hero.svelte';
	import Services from '../lib/components/services.svelte';
	import EmergencyBanner from '../lib/components/emergency-banner.svelte';
	import Pricing from '../lib/components/pricing.svelte';
	import ContactForm from '../lib/components/contact-form.svelte';
	import Footer from '../lib/components/footer.svelte';
	import FloatingCTA from '../lib/components/floating-cta.svelte';
	import Preloader from '../lib/components/preloader.svelte';

	let isLoading = $state(true);

	$effect(() => {
		const timer = setTimeout(() => {
			isLoading = false;
		}, 2000);
		return () => clearTimeout(timer);
	});
</script>

{#if isLoading}
	<Preloader />
{:else}
	<div class="fade-in">
		<Navbar />
		<Hero />
		<EmergencyBanner />
		<Services />
		<Pricing />
		<ContactForm />
		<Footer />
		<FloatingCTA />
	</div>
{/if}

<style>
	:global(body) {
		margin: 0;
		padding: 0;
		font-family: 'Geist', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
	}
</style>
