<script>
	import Call from '../icons/call.svelte';
	import Facebook from '../icons/facebook.svelte';
	import Instagram from '../icons/instagram.svelte';
	import Location from '../icons/location.svelte';
	import Mail from '../icons/mail.svelte';
	import MapPin from '../icons/mapPin.svelte';
	import Picture from '../icons/picture.svelte';
	import Tiktok from '../icons/tiktok.svelte';
	import Twitter from '../icons/twitter.svelte';

	let currentYear = new Date().getFullYear();
</script>

<div class="min-h-screen font-sans">
	<main class="flex gap-24 px-24 py-12">
		<div class="relative flex-1 rounded-3xl bg-red-100 p-12">
			<h1 class="mb-4 text-4xl font-bold text-red-600">Get in touch with us!</h1>
			<p class="mb-8 text-gray-600">
				Interested? Just pick up the phone to talk with our representative.
			</p>

			<div class="w-full py-8">
				<div class="h-72 w-full rounded-xl bg-gray-900"></div>
			</div>

			<button
				class="mt-6 rounded-md bg-red-600 px-6 py-3 font-medium text-white transition hover:bg-red-700"
				>Contact Veent</button
			>
		</div>

		<div class="flex flex-1 flex-col gap-12">
			<div>
				<h2 class="mb-4 text-3xl font-bold text-red-600">Locate Us</h2>
				<div class="mb-4 flex items-start gap-4">
					<Location />
					<p>2nd Floor, Lifestyle District,<br />Corrales Ext., Cagayan de Oro City 9000</p>
				</div>
				<a href="/" class="text-red-600 hover:underline">See Google Maps</a>
			</div>

			<div>
				<h2 class="mb-4 text-3xl font-bold text-red-600">Discover Veent</h2>
				<div class="flex flex-col gap-4">
					<div class="flex items-center gap-4">
						<Mail />
						<p>hello@veent.io</p>
					</div>
					<div class="flex items-center gap-4">
						<Call />
						<p>0985-890-8764<br />0956-760-0090</p>
					</div>
				</div>
				<div class="mt-6 flex gap-6">
					<a href="https://www.facebook.com/veent.io" class="text-red-600 hover:underline"
						><Facebook /></a
					>
					<a href="https://www.instagram.com/veentapps/#" class="text-red-600 hover:underline"
						><Instagram /></a
					>
					<a href="/" class="text-red-600 hover:underline"><Twitter /></a>
					<a href="/" class="text-red-600 hover:underline"><Tiktok /></a>
				</div>
			</div>

			<footer class="mt-auto text-sm text-gray-600">
				<p>Veent | All Rights Reserved {currentYear}</p>
			</footer>
		</div>
	</main>
</div>
