<script lang="ts">
	import { pageTabs } from '../../stores/userVariables';
	import Stream from '../icons/stream.svelte';

	let currentSlide = 0;
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

<div class="bg-[url('/background.png')] bg-cover bg-center h-screen w-full sm:bg-contain md:bg-cover relative min-h-screen overflow-hidden bg-gradient-to-b from-pink-50 to-orange-50">
	<!-- Background Blobs -->
	<div class="absolute left-[5%] top-[10%] h-4 w-4 rounded-full bg-pink-200/50" />
	<div class="absolute right-[10%] top-[15%] h-3 w-3 rounded-full bg-orange-200/50" />
	<div class="absolute bottom-[20%] left-[15%] h-5 w-5 rounded-full bg-red-200/50" />
	<div class="absolute bottom-[25%] right-[20%] h-4 w-4 rounded-full bg-pink-200/50" />

	<div class="mx-auto max-w-7xl px-4 py-16">
		<!-- Header -->
		<div class="text-center">
			<div class="text-red-500">Fast & Reliable</div>
			<h1 class="mt-4 text-4xl font-bold">Streamlined Attendance</h1>
			<p class="mx-auto mt-4 max-w-2xl text-gray-600">
				Simplify check-in with QR code scanning for quick and accurate guest verification.
			</p>
		</div>

		<!-- Center Image -->
		<div class="mt-16 flex items-center justify-center">
			<div class="flex w-full max-w-4xl justify-center">
				<div class="cursor-pointer transition-transform hover:scale-105" on:click={goBack}>
					<stream />
				</div>
			</div>
		</div>

		<!-- Navigation Controls -->
		<div class="mt-8 flex items-center justify-center gap-8">
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
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M15 19l-7-7 7-7"
					/>
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
	</div>
</div>
