<script lang="ts">
	const services = [
		{
			title: 'Light Duty Towing',
			icon: '🚗',
			description: 'Professional towing for cars and compact vehicles',
			image: 'https://images.unsplash.com/photo-1673187139211-1e7ec3dd60ec?fm=jpg&q=80&w=800&ixlib=rb-4.1.0'
		},
		{
			title: 'Medium Duty Towing',
			icon: '🚙',
			description: 'Heavy-duty towing for trucks and SUVs',
			image: 'https://images.unsplash.com/photo-1698998882426-39a6609ab10a?fm=jpg&q=80&w=800&ixlib=rb-4.1.0'
		},
		{
			title: 'Flat Tire Service',
			icon: '⚙️',
			description: 'Quick tire changes and professional repairs',
			image: 'https://plus.unsplash.com/premium_photo-1683141559021-3d1273fbb652?fm=jpg&q=80&w=800&ixlib=rb-4.1.0'
		},
		{
			title: 'Battery Jumpstart',
			icon: '🔋',
			description: 'Fast battery service and installation',
			image: 'https://images.unsplash.com/photo-1531746790731-6c087fecd51b?fm=jpg&q=80&w=800&ixlib=rb-4.1.0'
		},
		{
			title: 'Lockout Service',
			icon: '🔐',
			description: 'Quick professional lockout assistance',
			image: 'https://images.unsplash.com/photo-1558618666-fcd25c85cd64?fm=jpg&q=80&w=800&ixlib=rb-4.1.0'
		},
		{
			title: 'Wheel Lock Removal',
			icon: '🔧',
			description: 'Expert wheel lock and fastener removal',
			image: 'https://images.unsplash.com/photo-1487754180144-351b8ec7a630?fm=jpg&q=80&w=800&ixlib=rb-4.1.0'
		}
	];

	let hoveredIndex = $state(-1);
</script>

<section id="services" class="relative w-full py-24 bg-black-carbon border-t border-gray-medium">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<!-- Section Header -->
		<div class="text-center mb-16 slide-up">
			<h2 class="text-5xl md:text-6xl font-black mb-4 text-balance">
				<span class="chrome-text">OUR SERVICES</span>
			</h2>
			<p class="text-chrome text-xl">Fast, reliable roadside assistance when you need it most</p>
		</div>

		<!-- Services Grid -->
		<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
			{#each services as service, index (index)}
				<div
					class="group relative overflow-hidden rounded-lg border-2 border-purple-neon bg-gray-dark hover:bg-gray-medium transition-all duration-300 hover:scale-105 cursor-pointer purple-glow-hover chain-animation"
					onmouseenter={() => (hoveredIndex = index)}
					onmouseleave={() => (hoveredIndex = -1)}
				>
					<!-- Image Background -->
					<div class="absolute inset-0 opacity-30 group-hover:opacity-50 transition-opacity">
						<img
							src={service.image || "/placeholder.svg"}
							alt={service.title}
							class="w-full h-full object-cover"
						/>
					</div>

					<!-- Chrome Frame Effect -->
					<div class="absolute inset-0 border-4 border-chrome rounded-lg pointer-events-none"></div>

					<!-- Content -->
					<div class="relative z-10 p-8 flex flex-col justify-between h-full min-h-64">
						<div>
							<div class="text-5xl mb-4">{service.icon}</div>
							<h3 class="text-2xl font-black text-white mb-2">{service.title}</h3>
							<p class="text-chrome text-sm">{service.description}</p>
						</div>

						<!-- Hover Action -->
						{#if hoveredIndex === index}
							<div class="mt-4 slide-up">
								<a
									href="tel:+18168059240"
									class="inline-block px-6 py-2 bg-purple-neon text-white font-bold rounded purple-glow hover:bg-purple-glow transition"
								>
									Get Help Now →
								</a>
							</div>
						{/if}
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<style>
	section {
		background: linear-gradient(180deg, #0F0F0F 0%, #1A1A1A 100%);
	}
</style>
