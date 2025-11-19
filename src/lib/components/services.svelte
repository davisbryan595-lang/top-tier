<script lang="ts">
	const services = [
		{
			title: 'Light Duty Towing',
			icon: '🚗',
			description: 'Professional towing for cars and compact vehicles',
			image: 'https://images.unsplash.com/photo-1581578731548-c64695c952952?w=500&q=80'
		},
		{
			title: 'Medium Duty Towing',
			icon: '🚙',
			description: 'Heavy-duty towing for trucks and SUVs',
			image: 'https://images.unsplash.com/photo-1581578731548-c64695c952952?w=500&q=80'
		},
		{
			title: 'Flat Tire Service',
			icon: '⚙️',
			description: 'Quick tire changes and professional repairs',
			image: 'https://images.unsplash.com/photo-1583092917360-ce0dbafce850?w=500&q=80'
		},
		{
			title: 'Battery Jumpstart',
			icon: '🔋',
			description: 'Fast battery service and installation',
			image: 'https://images.unsplash.com/photo-1581092918056-0c4c3acd3789?w=500&q=80'
		},
		{
			title: 'Lockout Service',
			icon: '🔐',
			description: 'Quick professional lockout assistance',
			image: 'https://images.unsplash.com/photo-1593642632560-7348ab297866?w=500&q=80'
		},
		{
			title: 'Wheel Lock Removal',
			icon: '🔧',
			description: 'Expert wheel lock and fastener removal',
			image: 'https://images.unsplash.com/photo-1581092161562-40038e57e69f?w=500&q=80'
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
