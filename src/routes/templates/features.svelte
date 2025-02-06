<script lang="ts">
	import Smallblob from '$lib/smallblob.svelte';
	import { pageTabs } from '../../stores/userVariables';

	interface Feature {
		title: string;
		subtitle: string;
		route: string;
	}

	const features: Feature[] = [
		{ title: 'Effortless', subtitle: 'Event Pages', route: 'effortless' },
		{ title: 'Seamless', subtitle: 'Payments', route: 'seamless' },
		{ title: 'Smart', subtitle: 'Attendee Data', route: 'smart' },
		{ title: 'Streamlined', subtitle: 'Attendance', route: 'stream' },
		{ title: 'Data-Driven', subtitle: 'Decisions', route: 'data_driven' }
	];

	function handleFeatureClick(route: string): void {
		$pageTabs = route;
	}
</script>

<div class="relative my-[-20px] overflow-hidden">
	<div class="p-10 text-center">
		<h2 class="text-font text-[25px] font-bold text-red-500">Features</h2>
		<h1 class="text-font mt-px text-[35px] font-bold">
			Veent goes beyond basic<br />registration.
		</h1>
		<p class="text-font mb-100 mt- mx-auto max-w-2xl text-[#3F3D3E]">
			Our suite of features empowers you to create seamless<br /> event experiences. Choose a feature
			to see details.
		</p>

		<!-- Feature Blobs with Text -->
		<div class="relative mx-auto mt-px max-w-5xl">
			<!-- Effortless -->
			<button
				class="absolute left-[-10%] top-[-15%] cursor-pointer transition-transform hover:scale-105"
				on:click={() => handleFeatureClick('effortless')}
			>
				<div class="h-[200px] w-[200px] rounded-[40%]"><Smallblob /></div>
				<div class="absolute inset-0 flex flex-col items-center justify-center">
					<div class="text-[40px] font-bold ">Effortless</div>
					<div class="text-[20px] mt-[-10px]">Event Pages</div>
				</div>
			</button>

			<!-- Seamless -->
			<button
				class="absolute right-[-5%] top-[-5%] cursor-pointer transition-transform hover:scale-105"
				on:click={() => handleFeatureClick('seamless')}
			>
				<div class="h-[180px] w-[180px] rounded-[40%]"><Smallblob /></div>
				<div class="absolute inset-0 flex flex-col items-center justify-center">
					<div class="text-[40px] font-bold">Seamless</div>
					<div class="text-[20px] mt-[-10px]">Payments</div>
				</div>
			</button>

			<!-- Streamlined -->
			<button
				class="absolute left-[40%] top-[20%] cursor-pointer transition-transform hover:scale-105"
				on:click={() => handleFeatureClick('stream')}
			>
				<div class="h-[190px] w-[190px] rounded-[40%]"><Smallblob /></div>
				<div class="absolute inset-0 flex flex-col items-center justify-center">
					<div class="text-[40px] font-bold">Streamlined</div>
					<div class="text-[20px] mt-[-10px]">Attendance</div>
				</div>
			</button>

			<!-- Smart -->
			<button
				class="absolute left-[5%] top-[50%] cursor-pointer transition-transform hover:scale-105"
				on:click={() => handleFeatureClick('smart')}
			>
				<div class="h-[190px] w-[190px] rounded-[40%]"><Smallblob /></div>
				<div class="absolute inset-0 flex flex-col items-center justify-center">
					<div class="text-[40px] font-bold">Smart</div>
					<div class="text-[20px] mt-[-10px]">Attendee Data</div>
				</div>
			</button>

			<!-- Data-Driven -->
			<button
				class="absolute right-[9%] top-[55%] cursor-pointer transition-transform hover:scale-105"
				on:click={() => handleFeatureClick('data_driven')}
			>
				<div class="h-[180px] w-[180px] rounded-[40%]"><Smallblob /></div>
				<div class="absolute inset-0 flex flex-col items-center justify-center">
					<div class="text-[33px] font-bold">Data-Driven</div>
					<div class="text-[20px] mt-[-10px]">Decisions</div>
				</div>
			</button>

			<!-- Spacer div to maintain height -->
			<div class="h-[600px]"></div>
		</div>
	</div>
</div>

<style>
	@import url('https://fonts.googleapis.com/css2?family=SF+Pro+Display:wght@400;700&display=swap');

	/* .feature {
      @apply bg-gradient-to-r from-pink-300 to-orange-300 rounded-full p-6 shadow-lg;
    } */
	.text-font {
		font-family: 'SF Pro Display', sans-serif;
	}
</style>
