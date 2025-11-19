<script lang="ts">
</script>

<div class="fixed inset-0 bg-black-carbon flex items-center justify-center z-50 fade-in">
	<div class="text-center">
		<!-- Replace JSX comments with HTML comments -->
		<div class="mb-8 relative">
			<svg class="w-32 h-32 animate-spin" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
				<defs>
					<linearGradient id="chainGradient" x1="0%" y1="0%" x2="100%" y2="100%">
						<stop offset="0%" style="stop-color:#C0C0C0;stop-opacity:1" />
						<stop offset="100%" style="stop-color:#9D00FF;stop-opacity:1" />
					</linearGradient>
				</defs>
				<!-- Chain links -->
				<rect x="35" y="10" width="30" height="15" rx="7" fill="url(#chainGradient)" opacity="0.8" />
				<rect x="35" y="75" width="30" height="15" rx="7" fill="url(#chainGradient)" opacity="0.8" />
				<ellipse cx="50" cy="50" rx="35" ry="35" fill="none" stroke="url(#chainGradient)" stroke-width="3"
					opacity="0.6"
				/>
			</svg>
		</div>

		<!-- Loading Text -->
		<h1 class="text-4xl font-black chrome-text mb-4">TOP TIER</h1>
		<p class="text-2xl text-red-accent font-bold animate-pulse">Loading Rescue...</p>
	</div>
</div>

<style>
	div {
		background: linear-gradient(180deg, #0F0F0F 0%, #1A1A1A 100%);
	}
</style>
