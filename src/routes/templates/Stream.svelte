<script lang="ts">
	import { pageTabs } from '../../stores/userVariables';
	import Nav from '../icons/nav.svelte';
	import Stream from '../images/stream.svelte';

	function goBack() {
		$pageTabs = 'features';
	}
</script>

<div class="relative min-h-screen overflow-hidden">
	<!-- Background Blobs -->
	<div class="absolute left-[5%] top-[10%] h-4 w-4 rounded-full bg-pink-200/50" />
	<div class="absolute right-[10%] top-[15%] h-3 w-3 rounded-full bg-orange-200/50" />
	<div class="absolute bottom-[20%] left-[15%] h-5 w-5 rounded-full bg-red-200/50" />
	<div class="absolute bottom-[25%] right-[20%] h-4 w-4 rounded-full bg-pink-200/50" />

	<div class="mx-auto max-w-7xl px-4 py-16">
		<!-- Header -->
		<div class="text-center">
			<div class="text-2px text-[25px] font-bold text-[#D12F2B]">Fast & Reliable</div>
			<h1 class="mt-1 text-4xl font-bold">Streamlined Attendance</h1>
			<p class="mx-auto mt-3 max-w-2xl text-gray-600">
				Simplify check-in with QR code scanning for quick and accurate guest verification.
			</p>
		</div>

		<!-- Center Image -->
		<div class="mt-4 flex items-center justify-center">
			<div class="flex w-full max-w-4xl justify-center">
				<button class="cursor-pointer transition-transform hover:scale-105" on:click={goBack}>
					<Stream />
				</button>
			</div>
		</div>
		<!-- Navigation Controls -->

		<Nav />

	</div>
</div>