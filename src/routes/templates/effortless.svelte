<script lang="ts">
	import { pageTabs } from '../../stores/userVariables';
	import Effort from '../images/effort.svelte';
	import Navigation from './navigation.svelte';
	import Nav from '../icons/nav.svelte';

	// @ts-ignore
	function goBack() {
		$pageTabs = 'features';
	}
	
</script>
<Navigation />



<div class="">
	

	<!-- relative min-h-screen overflow-hidden bg-gradient-to-b from-pink-50 to-orange-50 -->
	<!-- Background Blobs -->
	<div class="absolute left-[5%] top-[10%] h-4 w-4 rounded-full bg-pink-200/50" />
	<div class="absolute right-[10%] top-[15%] h-3 w-3 rounded-full bg-orange-200/50" />
	<div class="absolute bottom-[20%] left-[15%] h-5 w-5 rounded-full bg-red-200/50" />
	<div class="absolute bottom-[25%] right-[20%] h-4 w-4 rounded-full bg-pink-200/50" />

	<div class="mx-auto max-w-7xl px-4 py-16 ">
		<!-- Header -->
		<div class="text-center">
			<div class="text-2px text-[25px] font-bold text-[#D12F2B]">Creativity</div>
			<h1 class="mt-2 text-4xl font-bold">Effortless Event Pages</h1>
			<p class="mx-auto mt-4 max-w-2xl text-gray-600">
				Design beautiful and informative event landing pages in minutes, no coding required.
			</p>
		</div>

		<!-- Center Image -->
		<div class="mt-16 flex items-center justify-center">
			<div class="flex w-full max-w-4xl justify-center">
				<button class="cursor-pointer transition-transform hover:scale-105" on:click={goBack}>
					<Effort />
				</button>
			</div>
		</div>

	

			<Nav/>
	</div>
</div>
