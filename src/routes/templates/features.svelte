<script lang="ts">
	import Smallblob from '$lib/smallblob.svelte';
	import { pageTabs } from '../../stores/userVariables';
	import Navigation from './navigation.svelte';

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

<div class="background">
	<Navigation />
	<div class="p-10 text-center">
		<h2 class="text-font text-3xl font-bold text-red-500">Features</h2>
		<h1 class="text-font mt-2 text-[30px] font-bold ">Veent goes beyond<br />basic registration.</h1>
		<p class="text-font mx-auto mb-16 mt-4 max-w-2xl text-gray-600">
			Our suite of features empowers you to create seamless event experiences. Choose a feature to
			see details.
		</p>

		<!-- Feature Blobs with Text -->
		<div class="relative mx-auto max-w-5xl">
			<!-- Effortless -->
			<div
				class="absolute left-[5%] top-[10%] cursor-pointer transition-transform hover:scale-105"
				on:click={() => handleFeatureClick('effortless')}
			>
				<div class="h-[200px] w-[200px] rounded-[40%] "><Smallblob/></div>
				<div class="absolute inset-0 flex flex-col items-center justify-center">
					<div class="text-[24px] font-bold">Effortless</div>
					<div class="text-[16px]">Event Pages</div>
				</div>
			</div>

			<!-- Seamless -->
			<div
				class="absolute right-[10%] top-[15%] cursor-pointer transition-transform hover:scale-105"
				on:click={() => handleFeatureClick('seamless')}
			>
				<div class="h-[180px] w-[180px] rounded-[40%]"><Smallblob/></div>
				<div class="absolute inset-0 flex flex-col items-center justify-center">
					<div class="text-[24px] font-bold">Seamless</div>
					<div class="text-[16px]">Payments</div>
				</div>
			</div>

			<!-- Streamlined -->
			<div
				class="absolute left-[35%] top-[40%] cursor-pointer transition-transform hover:scale-105"
				on:click={() => handleFeatureClick('stream')}
			>
				<div class="h-[190px] w-[190px] rounded-[40%]"><Smallblob/></div>
				<div class="absolute inset-0 flex flex-col items-center justify-center">
					<div class="text-[24px] font-bold">Streamlined</div>
					<div class="text-[16px]">Attendance</div>
				</div>
			</div>

			<!-- Smart -->
			<div
				class="absolute left-[10%] top-[60%] cursor-pointer transition-transform hover:scale-105"
				on:click={() => handleFeatureClick('smart')}
			>
				<div class="h-[190px] w-[190px] rounded-[40%]"><Smallblob/></div>
				<div class="absolute inset-0 flex flex-col items-center justify-center">
					<div class="text-[24px] font-bold">Smart</div>
					<div class="text-[16px]">Attendee Data</div>
				</div>
			</div>

			<!-- Data-Driven -->
			<div
				class="absolute right-[15%] top-[65%] cursor-pointer transition-transform hover:scale-105"
				on:click={() => handleFeatureClick('data_driven')}
			>
				<div class="h-[180px] w-[180px] rounded-[40%]"><Smallblob/></div>
				<div class="absolute inset-0 flex flex-col items-center justify-center">
					<div class="text-[24px] font-bold">Data-Driven</div>
					<div class="text-[16px]">Decisions</div>
				</div>
			</div>

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
