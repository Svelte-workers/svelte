<script>
	import Blob from "$lib/blob.svelte";
	import Navigation from './navigation.svelte';

	let currentYear = new Date().getFullYear();


	
</script>
<div class="background">
	<Navigation />

<div class="min-h-screen font-sans">
	<main class="max-w-5xl mx-auto py-16 px-8 text-center">
		<h1 class="text-red-600 text-4xl font-bold mb-4">Pricing</h1>
		<p class="text-gray-600 max-w-2xl mx-auto mb-12 leading-relaxed">
			Veent offers a robust suite of event management features completely free of charge, with a 5%
			transaction fee on ticket sales or products sold through the platform.
		</p>

		<div class="bg-white rounded-xl p-8 max-w-xl mx-auto shadow-lg">
			<div class="mb-8">
				<img src="/veent-logo.svg" alt="Veent" class="h-10 mx-auto mb-4" />
				<h2 class="text-gray-800 text-5xl font-bold text-start">Free</h2>
				<p class="text-gray-600 text-start">Free, no hidden charges</p>
			</div>

            <a href="https://www.veent.io/signup">
                <button class="w-full bg-red-600 text-white py-3 rounded-md text-lg font-medium transition">
                    Sign up now!
                </button>
            </a>

			<div class="text-left mt-8">

				<h3 class="text-gray-700 text-lg font-semibold mb-2">Experience these features for free:</h3>
				<ul class="text-gray-600 space-y-2">
					<li>☑ Customizable Registration Form</li>
					<li>☑ Personal QR Codes</li>
					<li>☑ QR Attendance</li>
					<li>☑ Certificate Generator</li>
					<li>☑ Raffle Draw from Attendance</li>
				</ul>

				<h3 class="text-gray-700 text-lg font-semibold mt-6 mb-2">Monetize your events with Veent:</h3>
				<ul class="text-gray-600 space-y-2">
					<li>☑ Merch Store</li>
					<li>☑ Paid Registration</li>
					<li>☑ Discount Voucher Generation</li>
				</ul>

				<h3 class="text-gray-700 text-lg font-semibold mt-6 mb-2">Collect fees with these features:</h3>
				<ul class="text-gray-600 space-y-2">
					<li>☑ Payment Processing Fee: 5% of transaction value</li>
				</ul>
			</div>
		</div>
	</main>
</div>
</div>
