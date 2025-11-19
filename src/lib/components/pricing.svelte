<script lang="ts">
	const prices = [
		{ name: 'Local Tow', price: '$75', description: 'Up to 10 miles' },
		{ name: 'Lockout', price: '$60', description: 'Professional service' },
		{ name: 'Tire Change', price: '$50', description: 'Flat tire assistance' },
		{ name: 'Jumpstart', price: '$65', description: 'Battery service' },
		{ name: 'Wheel Lock', price: '$100+', description: 'Removal service' },
		{ name: 'Long Distance', price: 'Call', description: 'Custom pricing' }
	];
</script>

<section id="pricing" class="relative w-full py-24 bg-black-carbon border-t border-gray-medium">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<!-- Section Header -->
		<div class="text-center mb-16 slide-up">
			<h2 class="text-5xl md:text-6xl font-black mb-4 text-balance">
				<span class="chrome-text">SIMPLE PRICING</span>
			</h2>
			<p class="text-chrome text-xl">No hidden fees, transparent rates</p>
		</div>

		<!-- Pricing Grid -->
		<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mb-12">
			{#each prices as price (price.name)}
				<div
					class="group relative p-8 rounded-lg border-3 border-chrome bg-gray-dark hover:border-purple-neon hover:bg-gray-medium transition-all duration-300 hover:shadow-2xl shine-effect"
				>
					<!-- Price Plate Chrome Effect -->
					<div class="absolute top-0 left-0 right-0 h-2 bg-gradient-to-r from-chrome-light via-chrome to-chrome-dark"></div>

					<h3 class="text-2xl font-black text-chrome mb-2">{price.name}</h3>
					<p class="text-4xl font-black text-red-accent mb-2">{price.price}</p>
					<p class="text-chrome text-sm">{price.description}</p>

					<div class="mt-6 pt-4 border-t border-chrome/50">
						<a
							href="tel:+18168059240"
							class="text-purple-neon hover:text-purple-glow font-bold transition"
						>
							Call for Details →
						</a>
					</div>
				</div>
			{/each}
		</div>

		<!-- Payment Methods -->
		<div class="text-center py-12 bg-gray-dark rounded-lg border-2 border-purple-neon">
			<h3 class="text-2xl font-black text-white mb-4">Payment Options</h3>
			<p class="text-chrome text-lg">💳 Cards • 📱 Cash App • 💰 Zelle • 💵 Cash</p>
		</div>
	</div>
</section>

<style>
	section {
		background: linear-gradient(180deg, #1A1A1A 0%, #0F0F0F 100%);
	}
</style>
