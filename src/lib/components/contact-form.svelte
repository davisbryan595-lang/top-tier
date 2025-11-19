<script lang="ts">
	let formData = $state({
		name: '',
		phone: '',
		location: '',
		vehicle: '',
		service: ''
	});

	function handleSubmit(e: Event) {
		e.preventDefault();
		alert(`Thank you! We'll dispatch help to ${formData.location} right away!`);
		formData = { name: '', phone: '', location: '', vehicle: '', service: '' };
	}
</script>

<section id="contact" class="relative w-full py-24 bg-black-carbon border-t border-gray-medium">
	<div class="max-w-3xl mx-auto px-4 sm:px-6 lg:px-8">
		<!-- Section Header -->
		<div class="text-center mb-12 slide-up">
			<h2 class="text-5xl md:text-6xl font-black mb-4 text-balance">
				<span class="chrome-text">GET DISPATCH NOW</span>
			</h2>
			<p class="text-chrome text-xl">Fill out the form or call us immediately</p>
		</div>

		<!-- Form -->
		<form onsubmit={handleSubmit} class="bg-gray-dark rounded-lg border-3 border-purple-neon p-8 carbon-fiber">
			<div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
				<input
					type="text"
					placeholder="Your Name"
					bind:value={formData.name}
					required
					class="px-4 py-3 bg-black-carbon border-2 border-chrome rounded text-white placeholder-chrome focus:outline-none focus:border-purple-neon transition"
				/>
				<input
					type="tel"
					placeholder="Your Phone"
					bind:value={formData.phone}
					required
					class="px-4 py-3 bg-black-carbon border-2 border-chrome rounded text-white placeholder-chrome focus:outline-none focus:border-purple-neon transition"
				/>
			</div>

			<div class="mb-6">
				<input
					type="text"
					placeholder="Current Location"
					bind:value={formData.location}
					required
					class="w-full px-4 py-3 bg-black-carbon border-2 border-chrome rounded text-white placeholder-chrome focus:outline-none focus:border-purple-neon transition"
				/>
			</div>

			<div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
				<input
					type="text"
					placeholder="Vehicle Make & Model"
					bind:value={formData.vehicle}
					class="px-4 py-3 bg-black-carbon border-2 border-chrome rounded text-white placeholder-chrome focus:outline-none focus:border-purple-neon transition"
				/>
				<select
					bind:value={formData.service}
					required
					class="px-4 py-3 bg-black-carbon border-2 border-chrome rounded text-chrome focus:outline-none focus:border-purple-neon transition"
				>
					<option value="">Select Service</option>
					<option value="towing">Light/Medium Towing</option>
					<option value="flat-tire">Flat Tire</option>
					<option value="battery">Battery Jumpstart</option>
					<option value="lockout">Lockout</option>
					<option value="wheel-lock">Wheel Lock Removal</option>
				</select>
			</div>

			<button
				type="submit"
				class="w-full py-4 bg-purple-neon text-white font-black text-lg rounded purple-glow hover:bg-purple-glow transition duration-300"
			>
				SEND DISPATCH 🚨
			</button>

			<p class="text-center text-chrome text-sm mt-4">Response time: Usually under 2 minutes</p>
		</form>

		<!-- Phone Highlights -->
		<div class="grid grid-cols-2 md:grid-cols-4 gap-4 mt-12">
			{#each ['816-805-9240', '816-805-9240', '816-805-9240', '816-805-9240'] as phone}
				<a
					href="tel:{phone}"
					class="p-4 bg-red-accent text-white font-black text-center rounded purple-glow-hover transition hover:bg-red-dark"
				>
					{phone}
				</a>
			{/each}
		</div>
	</div>
</section>

<style>
	section {
		background: linear-gradient(180deg, #0F0F0F 0%, #1A1A1A 100%);
	}
</style>
