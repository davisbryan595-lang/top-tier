<script lang="ts">
	let showCallout = $state(false);

	$effect(() => {
		const timer = setTimeout(() => {
			showCallout = true;
		}, 500);
		return () => clearTimeout(timer);
	});
</script>

<section id="home" class="relative w-full h-screen overflow-hidden bg-black-carbon">
	<!-- Background Image with Overlay -->
	<div class="absolute inset-0">
		<img
			src="https://images.unsplash.com/photo-1449824913935-59a10b8d2000?w=1920&q=80"
			alt="Towing truck on highway"
			class="w-full h-full object-cover opacity-20"
		/>
		<div class="absolute inset-0 bg-gradient-to-b from-black-carbon via-transparent to-black-carbon"></div>
	</div>

	<!-- Animated Carbon Fiber Overlay -->
	<div class="absolute inset-0 carbon-fiber opacity-5"></div>

	<!-- Content -->
	<div class="relative z-10 h-full flex flex-col items-center justify-center px-4">
		<div class="text-center slide-up">
			<!-- Logo -->
			<div class="mb-8 animate-bounce" style="animation-duration: 3s;">
				<img
					src="https://hebbkx1anhila5yf.public.blob.vercel-storage.com/top2-EHYTkCqOssSZhr2aHXCRC5QAZSM7Ny.jpg"
					alt="Top Tier Towing"
					class="h-32 w-auto mx-auto shine-effect"
				/>
			</div>

			<!-- Main Heading -->
			<h1 class="text-6xl md:text-7xl font-black mb-4 text-balance">
				<span class="chrome-text">TOP TIER</span>
				<br />
				<span class="text-red-accent font-black text-5xl md:text-6xl">TOWING</span>
			</h1>

			<!-- Slogan -->
			{#if showCallout}
				<p class="text-2xl md:text-3xl text-red-accent font-bold mb-12 slide-up">
					Faster Than Your Insurance Company
				</p>
			{/if}

			<!-- CTA Buttons -->
			<div class="flex flex-col sm:flex-row gap-4 justify-center mb-12">
				<a
					href="tel:+18168059240"
					class="px-8 py-4 bg-purple-neon text-white font-bold rounded-lg purple-glow hover:bg-purple-glow transition duration-300 flex items-center justify-center gap-2 text-lg"
				>
					<svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
						<path d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"
						></path>
					</svg>
					CALL NOW: 816-805-9240
				</a>
				<button
					class="px-8 py-4 bg-red-accent text-white font-bold rounded-lg red-glow hover:bg-red-dark transition duration-300 text-lg"
				>
					Get Towed Now
				</button>
			</div>

			<!-- Emergency Badge -->
			<div class="inline-block px-6 py-3 bg-purple-neon/20 border-2 border-purple-neon rounded-full">
				<p class="text-purple-neon font-bold text-lg">🚨 24/7 EMERGENCY SERVICE</p>
			</div>
		</div>
	</div>

	<!-- Scroll Indicator -->
	<div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 z-10 animate-bounce">
		<svg class="w-6 h-6 text-purple-neon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
			<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"
			></path>
		</svg>
	</div>
</section>

<style>
	section {
		background: linear-gradient(180deg, #0F0F0F 0%, #1A1A1A 100%);
	}
</style>
