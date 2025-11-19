<script lang="ts">
	let selectedImage = $state(0);
	let isExpanded = $state(false);

	const galleryImages = [
		{
			url: 'https://images.unsplash.com/photo-1488646953014-85cb44e25828?w=1200&q=80',
			alt: 'Professional Towing Truck',
			title: 'Heavy Duty Towing'
		},
		{
			url: 'https://images.unsplash.com/photo-1469854523086-cc02fe5d8800?w=1200&q=80',
			alt: 'Roadside Assistance',
			title: 'Emergency Response'
		},
		{
			url: 'https://images.unsplash.com/photo-1552519507-da3a142e8e8d?w=1200&q=80',
			alt: 'Car Recovery Service',
			title: 'Vehicle Recovery'
		},
		{
			url: 'https://images.unsplash.com/photo-1464207687429-7505649dae38?w=1200&q=80',
			alt: 'Flatbed Towing',
			title: 'Flatbed Transport'
		},
		{
			url: 'https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=1200&q=80',
			alt: 'Motorcycle Towing',
			title: 'Motorcycle Towing'
		},
		{
			url: 'https://images.unsplash.com/photo-1485846234645-a62644f84728?w=1200&q=80',
			alt: 'Night Operations',
			title: '24/7 Service'
		}
	];

	function nextImage() {
		selectedImage = (selectedImage + 1) % galleryImages.length;
	}

	function prevImage() {
		selectedImage = (selectedImage - 1 + galleryImages.length) % galleryImages.length;
	}
</script>

<section id="gallery" class="relative w-full py-24 bg-black-carbon">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<!-- Section Header -->
		<div class="text-center mb-16 slide-up">
			<h2 class="text-5xl md:text-6xl font-black mb-4 text-balance">
				<span class="chrome-text">OUR WORK</span>
			</h2>
			<p class="text-chrome text-xl">Professional towing and recovery in action</p>
		</div>

		<!-- Main Gallery Display -->
		<div class="relative mb-12 group">
			<!-- Main featured image with chrome border and glow effect -->
			<div class="relative rounded-xl overflow-hidden border-4 border-purple-neon shadow-lg shadow-purple-neon/30 hover:shadow-purple-neon/50 transition-shadow duration-300">
				<img
					src={galleryImages[selectedImage].url || "/placeholder.svg"}
					alt={galleryImages[selectedImage].alt}
					class="w-full h-auto aspect-video object-cover"
				/>
				<div class="absolute inset-0 bg-gradient-to-t from-black/60 via-transparent to-transparent pointer-events-none"></div>
				
				<!-- Image Title Overlay -->
				<div class="absolute bottom-0 left-0 right-0 p-8 text-white">
					<h3 class="text-3xl md:text-4xl font-black mb-2">{galleryImages[selectedImage].title}</h3>
					<p class="text-chrome text-lg">Professional service you can trust</p>
				</div>
			</div>

			<!-- Navigation Arrows -->
			<button
				onclick={prevImage}
				class="absolute left-4 top-1/2 -translate-y-1/2 z-10 w-12 h-12 rounded-full bg-purple-neon hover:bg-purple-glow text-black font-bold text-2xl transition-all duration-300 hover:scale-110 shadow-lg"
				aria-label="Previous image"
			>
				←
			</button>
			<button
				onclick={nextImage}
				class="absolute right-4 top-1/2 -translate-y-1/2 z-10 w-12 h-12 rounded-full bg-purple-neon hover:bg-purple-glow text-black font-bold text-2xl transition-all duration-300 hover:scale-110 shadow-lg"
				aria-label="Next image"
			>
				→
			</button>

			<!-- Image Counter -->
			<div class="absolute top-4 right-4 bg-black/80 backdrop-blur px-4 py-2 rounded-full border-2 border-chrome text-chrome font-black">
				{selectedImage + 1} / {galleryImages.length}
			</div>
		</div>

		<!-- Thumbnail Grid -->
		<div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-4 mb-12">
			{#each galleryImages as image, index (index)}
				<button
					onclick={() => (selectedImage = index)}
					class={`group relative rounded-lg overflow-hidden border-3 transition-all duration-300 cursor-pointer hover:scale-105 ${
						selectedImage === index
							? 'border-purple-neon shadow-lg shadow-purple-neon/50'
							: 'border-chrome'
					}`}
					aria-label="Gallery thumbnail {index + 1}"
				>
					<img src={image.url || "/placeholder.svg"} alt={image.alt} class="w-full h-24 object-cover" />
					<div class="absolute inset-0 bg-black/40 group-hover:bg-black/20 transition-all duration-300"></div>
					<div class="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300">
						<div class="text-2xl">▶</div>
					</div>
				</button>
			{/each}
		</div>

		<!-- Gallery Stats -->
		<div class="grid grid-cols-1 md:grid-cols-3 gap-8 py-12 border-t-2 border-chrome/30">
			<div class="text-center slide-up">
				<h4 class="text-5xl font-black text-red-accent mb-2">500+</h4>
				<p class="text-chrome text-lg">Successful Recoveries</p>
			</div>
			<div class="text-center slide-up">
				<h4 class="text-5xl font-black text-red-accent mb-2">24/7</h4>
				<p class="text-chrome text-lg">Always Ready to Help</p>
			</div>
			<div class="text-center slide-up">
				<h4 class="text-5xl font-black text-red-accent mb-2">99%</h4>
				<p class="text-chrome text-lg">Customer Satisfaction</p>
			</div>
		</div>
	</div>
</section>

<style>
	section {
		background: linear-gradient(180deg, #0F0F0F 0%, #1A1A1A 100%);
	}
</style>
