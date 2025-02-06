<!-- TEXT COLOR
#333A3F 
-->

<script>
	import ContactBlob from '$lib/contactBlob.svelte';
	import Smallblob from '$lib/smallblob.svelte';
	import Call from '../icons/call.svelte';
	import Contactus from '../icons/contactus.svelte';
	import Contactusblob from '../icons/contactusblob.svelte';
	import Facebook from '../icons/facebook.svelte';
	import Instagram from '../icons/instagram.svelte';
	import Location from '../icons/location.svelte';
	import Mail from '../icons/mail.svelte';
	import MapPin from '../icons/mapPin.svelte';
	import Picture from '../icons/picture.svelte';
	import Tiktok from '../icons/tiktok.svelte';
	import Twitter from '../icons/twitter.svelte';
	import Navigation from './navigation.svelte';

	let currentYear = new Date().getFullYear();
	
	
</script>

<div class="background relative overflow-hidden">
	<!-- Upper right circle -->
	<div
		class="absolute -right-60 -top-60 h-[600px] w-[600px] rounded-full bg-[#D12B7A] opacity-20 blur-[100px]"
	></div>

	<!-- Lower left circle -->
	<div
		class="absolute -bottom-60 -left-60 h-[600px] w-[600px] rounded-full bg-[#D1822B] opacity-20 blur-[100px]"
	></div>

	<Navigation />
	<div class="w-full px-4 md:px-8 lg:px-24">
		<!-- Added responsive padding -->
		<main class="flex flex-col gap-8 py-8 lg:flex-row lg:gap-24 lg:py-12">
			<!-- Made flex column on mobile -->
			<div class="relative flex-1 rounded-3xl p-6 lg:p-12">
				<!-- Blob added here and positioned behind content -->
				<ContactBlob class="absolute inset-0 left-0 top-0 -z-10 h-[80%] w-[80%]" />

				<h1 class="mb-4 text-3xl font-bold text-red-600 lg:text-4xl">Get in touch with us!</h1>
				<p class="mb-8 text-lg text-gray-600">
					Interested? Just pick up the phone to talk with our representative.
				</p>

				<div class="lg: w-full lg:ps-16">
					<Contactus />
				</div>
<div class="">
	<main class="flex px-24 py-12 gap-24">
		<div class="flex-1 bg-blue-100 rounded-3xl p-12 relative"> 
			<h1 class="text-red-600 text-4xl font-bold mb-4">Get in touch with us!</h1>
			<p class="text-gray-600 mb-8">Interested? Just pick up the phone to talk with our representative.</p>

			<div class="w-full py-8">
				<div class="w-full h-72 bg-gray-900 rounded-xl"></div>
				
			</div>

				<div class="mt-4 flex justify-center">
					<button
						class="w-full rounded-full bg-red-600 px-16 py-3 font-medium text-white transition hover:bg-red-700 lg:w-auto"
					>
						Contact Veent
					</button>
				</div>
			</div>

			<div class="flex flex-1 flex-col gap-6 lg:gap-10">
				<!-- Locate us section -->
				<div class="">
					<h2 class="mb-4 text-2xl font-extrabold text-red-600 lg:text-[32px]">Locate Us</h2>
					<div class="mb-4 flex flex-col items-start gap-4 sm:flex-row">
						<Location />
						<p class="text-sm lg:text-lg">
							2nd Floor, Lifestyle District,<br />Corrales Ext., Cagayan de Oro City 9000
						</p>
					</div>
					<a
						href="https://maps.app.goo.gl/AhQTjuzHmd3HS1VN8"
						class="inline-flex items-center gap-2 text-red-600 transition-all duration-300 ease-in-out hover:gap-3 hover:text-red-700"
					>
						See Google Maps
						<svg
							xmlns="http://www.w3.org/2000/svg"
							width="20"
							height="20"
							viewBox="0 0 24 24"
							fill="none"
							stroke="currentColor"
							stroke-width="2"
							stroke-linecap="round"
							stroke-linejoin="round"
							class="transition-transform duration-300 group-hover:translate-x-1"
						>
							<path d="m9 18 6-6-6-6" />
						</svg>
					</a>
					<div class="my-8 h-[1px] w-full bg-gray-200"></div>
				</div>

				<div class="p-2">
					<h2 class="mb-4 text-2xl font-bold text-red-600 lg:text-[32px]">Discover Veent</h2>
					<div class="flex flex-col gap-2">
						<div class="flex items-center gap-4">
							<Mail />
							<p class="text-sm font-medium lg:text-lg">hello@veent.io</p>
						</div>
						<div class="flex items-center gap-4">
							<Call />
							<p class="text-sm font-medium lg:text-lg">0985-890-8764<br />0956-760-0090</p>
						</div>
					</div>
					<div class="mt-6 flex gap-6">
						<a
							href="https://www.facebook.com/veent.io"
							class="text-red-600 transition-transform duration-300 ease-in-out hover:scale-110 hover:underline"
							><Facebook /></a
						>
						<a
							href="https://www.instagram.com/veentapps/#"
							class="text-red-600 transition-transform duration-300 ease-in-out hover:scale-110 hover:underline"
							><Instagram /></a
						>
						<a
							href="/"
							class="text-red-600 transition-transform duration-300 ease-in-out hover:scale-110 hover:underline"
							><Twitter /></a
						>
						<a
							href="/"
							class="text-red-600 transition-transform duration-300 ease-in-out hover:scale-110 hover:underline"
							><Tiktok /></a
						>
					</div>
				</div>

				<footer class="mt-auto text-xs text-gray-600 lg:text-sm">
					<p>Veent | All Rights Reserved {currentYear}</p>
				</footer>
			</div>
		</main>
	</div>
</div>
