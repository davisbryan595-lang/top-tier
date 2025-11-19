<script lang="ts">
	let mobileMenuOpen = $state(false);
</script>

<nav class="fixed top-0 w-full z-50 carbon-fiber border-b border-gray-medium bg-opacity-95 backdrop-blur">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="flex justify-between items-center h-20">
			<!-- Replace JSX comments with HTML comments -->
			<div class="flex items-center gap-2 shine-effect">
				<img
					src="https://hebbkx1anhila5yf.public.blob.vercel-storage.com/top2-EHYTkCqOssSZhr2aHXCRC5QAZSM7Ny.jpg"
					alt="Top Tier Towing Logo"
					class="h-16 w-auto"
				/>
			</div>

			<!-- Desktop Menu -->
			<div class="hidden md:flex gap-8">
				<a href="#home" class="text-chrome hover:text-purple-neon transition duration-300">Home</a>
				<a href="#services" class="text-chrome hover:text-purple-neon transition duration-300">Services</a>
				<a href="#pricing" class="text-chrome hover:text-purple-neon transition duration-300">Pricing</a>
				<a href="#contact" class="text-chrome hover:text-purple-neon transition duration-300">Contact</a>
			</div>

			<!-- Mobile Menu Button -->
			<button
				class="md:hidden text-chrome hover:text-purple-neon transition"
				onclick={() => (mobileMenuOpen = !mobileMenuOpen)}
			>
				<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"
					></path>
				</svg>
			</button>
		</div>

		<!-- Mobile Menu -->
		{#if mobileMenuOpen}
			<div class="md:hidden pb-4 space-y-2">
				<a href="#home" class="block text-chrome hover:text-purple-neon py-2">Home</a>
				<a href="#services" class="block text-chrome hover:text-purple-neon py-2">Services</a>
				<a href="#pricing" class="block text-chrome hover:text-purple-neon py-2">Pricing</a>
				<a href="#contact" class="block text-chrome hover:text-purple-neon py-2">Contact</a>
			</div>
		{/if}
	</div>
</nav>

<style>
	nav {
		background: rgba(15, 15, 15, 0.95);
	}
</style>
