<script>
	import CirclesLeft from '$lib/circles-left.svelte';
	import CirclesRight from '$lib/circles-right.svelte';
	import HomeBlob from '$lib/homeBlob.svelte';
	import Navigation from './navigation.svelte';
</script>

<div class="">
	<CirclesLeft />
</div>

<div class="">
	<CirclesRight />
</div>
<Navigation/>
<div class="flex min-h-screen items-center justify-center">
	
	<div class="fade-down relative flex flex-col items-center justify-center text-center">
		
		<!-- Blob Positioned Behind Everything -->
		<div class="absolute inset-0 z-[-1] flex items-center justify-center">
			<HomeBlob />
		</div>

		<!-- Veent Image -->
		<img class="relative z-10 mt-[-160px] h-[120px] w-[350px]" src="/veent.png" alt="veent" />

		<!-- Main Text Content -->
		<div class="mt-2 text-[28px] font-bold text-[#D12F2B]">Events, simplified.</div>
		<div class="mt-2 w-[650px] text-center text-[20px] text-black">
			Streamline event registration with Veent. Our user-friendly web app makes creating events a
			breeze. Packed with features and affordable pricing, Veent simplifies event management for
			everyone.
		</div>

		<!-- Call-to-action Button -->
		<div class="my-[40px]">
			<a href="https://www.veent.io/signup">
				<button
					class="rounded-[10px] bg-[#D12F2B] px-[40px] py-2 text-[16px] font-bold text-white transition hover:bg-[#990C08]"
				>
					Sign up for free!
				</button>
			</a>
		</div>
	</div>
</div>