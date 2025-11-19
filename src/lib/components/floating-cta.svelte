<script lang="ts">
	let isVisible = $state(true);
</script>

<div class="fixed bottom-6 right-6 z-40 float">
	<a
		href="tel:+18168059240"
		class="flex items-center justify-center w-16 h-16 bg-red-accent text-white rounded-full font-black text-2xl hover:bg-red-dark transition duration-300 red-glow hover:shadow-2xl"
	>
		📞
	</a>
</div>

<style>
	div {
		animation: float 3s ease-in-out infinite;
	}
</style>
