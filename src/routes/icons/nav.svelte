<script lang="ts">
	import { pageTabs } from '../../stores/userVariables';

	let currentSlide = 3;
	const totalSlides = 5;

	function nextSlide() {
		currentSlide = (currentSlide + 1) % totalSlides;
	}

	function prevSlide() {
		currentSlide = (currentSlide - 1 + totalSlides) % totalSlides;
	}

	function goToSlide(index: number) {
		currentSlide = index;
	}

	function goBack() {
		$pageTabs = 'features';
	}
</script>

<!-- Navigation Controls -->
<div class=" item-center mt-8 flex items-center justify-center gap-8">
	<button
		class="rounded-full bg-red-500 p-3 text-white transition hover:bg-red-600"
		on:click={prevSlide}
	>
		<svg
			xmlns="http://www.w3.org/2000/svg"
			class="h-6 w-6"
			fill="none"
			viewBox="0 0 24 24"
			stroke="currentColor"
		>
			<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
		</svg>
	</button>

	<!-- Navigation Dots -->
	<div class="flex space-x-2">
		{#each Array(totalSlides) as _, i}
			<button
				class="h-2 w-2 rounded-full transition-all {currentSlide === i
					? 'w-4 bg-red-500'
					: 'bg-gray-300'}"
				on:click={() => goToSlide(i)}
			/>
		{/each}
	</div>

	<button
		class="rounded-full bg-red-500 p-3 text-white transition hover:bg-red-600"
		on:click={nextSlide}
	>
		<svg
			xmlns="http://www.w3.org/2000/svg"
			class="h-6 w-6"
			fill="none"
			viewBox="0 0 24 24"
			stroke="currentColor"
		>
			<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
		</svg>
	</button>
</div>
