<script>
	import CirclesLeft from '$lib/circles-left.svelte';
	import CirclesRight from '$lib/circles-right.svelte';
	import CirclesPricing from '$lib/circlesPricing.svelte';
	import PricingBlob from '$lib/pricingBlob.svelte';
	CirclesRight;

	let currentYear = new Date().getFullYear();
</script>

<div class="min-h-screen font-sans">
	<main class="mx-auto max-w-5xl px-8 py-16 text-center">
		<h1 class="mb-4 text-4xl font-bold text-red-600">Pricing</h1>
		<p class="mx-auto mb-12 max-w-2xl leading-relaxed text-gray-600">
			Veent offers a robust suite of event management features completely free of charge, with a 5%
			transaction fee on ticket sales or products sold through the platform.
		</p>

		<div class="mx-auto max-w-xl rounded-xl border-[1px] border-[#F3CCCF] bg-white p-8 shadow-lg">
			<div class="mb-8">
				<img src="/veent-logo.svg" alt="Veent" class="mx-auto mb-4 h-10" />
				<h2 class="text-start text-5xl font-bold text-gray-800">Free</h2>
				<p class="text-start text-gray-600">Free, no hidden charges</p>
			</div>

			<a href="https://www.veent.io/signup">
				<button class="w-full rounded-md bg-red-600 py-3 text-lg font-medium text-white transition">
					Sign up now!
				</button>
			</a>

			<div class="">
				<CirclesPricing />
			</div>

			<div class="absolute inset-1 z-[-1] p-[50px]">
				<PricingBlob />
			</div>

			<div class="mt-8 text-left">
				<h3 class="mb-2 text-lg font-semibold text-gray-700">
					Experience these features for free:
				</h3>
				<ul class="space-y-2 text-gray-600">
					<li>☑ Customizable Registration Form</li>
					<li>☑ Personal QR Codes</li>
					<li>☑ QR Attendance</li>
					<li>☑ Certificate Generator</li>
					<li>☑ Raffle Draw from Attendance</li>
				</ul>

				<h3 class="mb-2 mt-6 text-lg font-semibold text-gray-700">
					Monetize your events with Veent:
				</h3>
				<ul class="space-y-2 text-gray-600">
					<li>☑ Merch Store</li>
					<li>☑ Paid Registration</li>
					<li>☑ Discount Voucher Generation</li>
				</ul>

				<h3 class="mb-2 mt-6 text-lg font-semibold text-gray-700">
					Collect fees with these features:
				</h3>
				<ul class="space-y-2 text-gray-600">
					<li>☑ Payment Processing Fee: 5% of transaction value</li>
				</ul>
			</div>
		</div>
	</main>
</div>
