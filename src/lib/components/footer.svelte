<script lang="ts">
	const currentYear = new Date().getFullYear();
</script>

<footer class="relative w-full bg-black-carbon carbon-fiber border-t-4 border-purple-neon">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
		<div class="grid grid-cols-1 md:grid-cols-3 gap-12 mb-12">
			<!-- Company Info -->
			<div>
				<h3 class="text-2xl font-black text-chrome mb-4">TOP TIER TOWING</h3>
				<p class="text-chrome mb-4">24/7 Emergency Towing & Recovery</p>
				<p class="text-chrome text-sm">Independence, MO & Surrounding Areas</p>
			</div>

			<!-- Contact -->
			<div>
				<h3 class="text-xl font-black text-purple-neon mb-4">CONTACT US</h3>
				<div class="space-y-2">
					<a href="tel:+18168059240" class="text-chrome hover:text-purple-neon transition block">
						📞 +1 816-805-9240
					</a>
					<a href="mailto:toptiertowkc@gmail.com" class="text-chrome hover:text-purple-neon transition block">
						✉️ toptiertowkc@gmail.com
					</a>
					<p class="text-chrome text-sm">🕐 Available 24/7/365</p>
				</div>
			</div>

			<!-- Quick Links -->
			<div>
				<h3 class="text-xl font-black text-red-accent mb-4">QUICK LINKS</h3>
				<div class="space-y-2">
					<a href="#services" class="text-chrome hover:text-red-accent transition block">Services</a>
					<a href="#pricing" class="text-chrome hover:text-red-accent transition block">Pricing</a>
					<a href="#contact" class="text-chrome hover:text-red-accent transition block">Contact</a>
					<a href="tel:+18168059240" class="text-chrome hover:text-red-accent transition block"
						>Emergency Call</a
					>
				</div>
			</div>
		</div>

		<!-- Divider -->
		<div class="border-t border-chrome/30 my-8"></div>

		<!-- Bottom Footer -->
		<div class="flex flex-col md:flex-row justify-between items-center text-chrome text-sm">
			<p>&copy; {currentYear} Top Tier Towing & Recovery LLC. All rights reserved.</p>
			<p>🚗 Faster Than Your Insurance Company 🚗</p>
		</div>
	</div>
</footer>

<style>
	footer {
		background: linear-gradient(180deg, #1A1A1A 0%, #0F0F0F 100%);
	}
</style>
