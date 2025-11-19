<script lang="ts">
	let isFlashing = $state(true);
</script>

<div class="relative w-full bg-gradient-to-r from-red-accent to-purple-neon overflow-hidden py-4">
	<div class="flex items-center justify-center gap-4 text-white font-black text-2xl md:text-4xl text-balance">
		<svg class="w-8 h-8 md:w-10 md:h-10 animate-spin" fill="currentColor" viewBox="0 0 24 24">
			<circle cx="12" cy="12" r="1" />
			<circle cx="19" cy="5" r="1" opacity="0.3" />
			<circle cx="5" cy="19" r="1" opacity="0.3" />
		</svg>
		24/7 EMERGENCY TOWING — WE'RE ALREADY ON THE WAY
		<svg class="w-8 h-8 md:w-10 md:h-10 animate-spin" fill="currentColor" viewBox="0 0 24 24">
			<circle cx="12" cy="12" r="1" />
			<circle cx="19" cy="5" r="1" opacity="0.3" />
			<circle cx="5" cy="19" r="1" opacity="0.3" />
		</svg>
	</div>
	<div class="absolute inset-0 bg-gradient-to-r from-transparent via-white to-transparent opacity-20 animate-pulse"></div>
</div>

<style>
	div {
		animation: pulse 2s infinite;
	}

	@keyframes pulse {
		0%, 100% {
			opacity: 1;
		}
		50% {
			opacity: 0.8;
		}
	}
</style>
