<script lang="ts">
	import Blob from '$lib/pricingBlob.svelte';
	import { pageTabs } from '../../stores/userVariables';
	import Nav from '../icons/nav.svelte';
	import Seam from '../images/seam.svelte';
	import Seamless from '../images/seamless.svelte';

	function goBack() {
		$pageTabs = 'features';
	}
</script>

<div class="relative overflow-hidden">
	<!-- Background Blobs -->
	<div class="absolute left-[5%] top-[10%] h-4 w-4 rounded-full bg-pink-200/50" />
	<div class="absolute right-[10%] top-[15%] h-3 w-3 rounded-full bg-orange-200/50" />
	<div class="absolute bottom-[20%] left-[15%] h-5 w-5 rounded-full bg-red-200/50" />
	<div class="absolute bottom-[25%] right-[20%] h-4 w-4 rounded-full bg-pink-200/50" />

	<div class="mx-auto max-w-7xl px-4 py-16">
		<!-- Header -->
		<div class="text-center">
			<div class="text-2px text-[25px] font-bold text-[#D12F2B]">Convenience</div>
			<h1 class="mt-0 text-[40px] font-bold">Seamless Payments</h1>
			<p class="text=[16px] mx-auto mt-1 max-w-2xl text-[#3F3D3E]">
				Accept registrations with integrated payment processing for a smooth and secure experience.
				<span class="text=[16px] text-bold text-[16px] italic text-[#3F3D3E]"
					>(additional fees may apply)</span
				>
			</p>
		</div>

		<!-- Center Image -->
		<div class="mt-5 flex items-center justify-center">
			<div class="flex w-full max-w-4xl justify-center">
				<button class="cursor-pointer transition-transform hover:scale-105" on:click={goBack}>
					<Seamless />
				</button>
			</div>
		</div>

		<div class="mt-5 text-center text-[17px]">
			<p>Can also accept payment installment via</p>
			<div class=" item-center mt-5 flex justify-center">
				<Seam />
			</div>
		</div>

		<!-- Navigation Controls -->
		<Nav />
	</div>
</div>
