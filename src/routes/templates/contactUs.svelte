<script>
	import Call from "../icons/call.svelte";
	import Facebook from "../icons/facebook.svelte";
	import Instagram from "../icons/instagram.svelte";
	import Location from "../icons/location.svelte";
	import Mail from "../icons/mail.svelte";
	import MapPin from "../icons/mapPin.svelte";
	import Picture from "../icons/picture.svelte";
	import Tiktok from "../icons/tiktok.svelte";
	import Twitter from "../icons/twitter.svelte";
	import Navigation from './navigation.svelte';
    
	let currentYear = new Date().getFullYear();
</script>
<div class="background">
	<Navigation />
<div class="">
	<main class="flex px-24 py-12 gap-24">
		<div class="flex-1 bg-red-100 rounded-3xl p-12 relative">
			<h1 class="text-red-600 text-4xl font-bold mb-4">Get in touch with us!</h1>
			<p class="text-gray-600 mb-8">Interested? Just pick up the phone to talk with our representative.</p>

			<div class="w-full py-8">
				<div class="w-full h-72 bg-gray-900 rounded-xl"></div>
				
			</div>

			<button class="bg-red-600 text-white py-3 px-6 rounded-md font-medium mt-6 hover:bg-red-700 transition">Contact Veent</button>
		</div>

		<div class="flex-1 flex flex-col gap-12">
			<div>
				<h2 class="text-red-600 text-3xl font-bold mb-4">Locate Us</h2>
				<div class="flex gap-4 items-start mb-4">
					<Location/>
					<p>2nd Floor, Lifestyle District,<br />Corrales Ext., Cagayan de Oro City 9000</p>
				</div>
				<a href="/" class="text-red-600 hover:underline">See Google Maps</a>
			</div>

			<div>
				<h2 class="text-red-600 text-3xl font-bold mb-4">Discover Veent</h2>
				<div class="flex flex-col gap-4">
					<div class="flex gap-4 items-center">
                        <Mail/>
						<p>hello@veent.io</p>
					</div>
					<div class="flex gap-4 items-center">
						<Call/>
						<p>0985-890-8764<br />0956-760-0090</p>
					</div>
				</div>
				<div class="flex gap-6 mt-6">
					<a href="https://www.facebook.com/veent.io" class="text-red-600 hover:underline"><Facebook/></a>
					<a href="https://www.instagram.com/veentapps/#" class="text-red-600 hover:underline"><Instagram/></a>
					<a href="/" class="text-red-600 hover:underline"><Twitter/></a>
					<a href="/" class="text-red-600 hover:underline"><Tiktok/></a>
				</div>
			</div>

			<footer class="mt-auto text-gray-600 text-sm">
				<p>Veent | All Rights Reserved {currentYear}</p>
			</footer>
		</div>
	</main>
</div>
</div>
