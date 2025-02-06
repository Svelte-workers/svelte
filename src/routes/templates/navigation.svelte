<script>
	import { pageTabs } from '../../stores/userVariables';
	let isOpen = false;

	const tabs = [
		{ name: 'home', label: 'Home' },
		{ name: 'aboutUs', label: 'About Us' },
		{ name: 'features', label: 'Features' },
		{ name: 'pricing', label: 'Pricing' },
		{ name: 'contactUs', label: 'Kontaka dri' }
	];
</script>

<nav class="mx-6 flex items-center justify-between p-4">
	<!-- Logo -->
	<div>
		<img class="w-24" src="/veent-logo.svg" alt="veent" />
	</div>

	<!-- Mobile Menu Button -->
	<button class="block text-black focus:outline-none lg:hidden" on:click={() => (isOpen = !isOpen)}>
		<svg
			class="h-8 w-8"
			fill="none"
			stroke="currentColor"
			viewBox="0 0 24 24"
			xmlns="http://www.w3.org/2000/svg"
		>
			<path
				stroke-linecap="round"
				stroke-linejoin="round"
				stroke-width="2"
				d={isOpen ? 'M6 18L18 6M6 6l12 12' : 'M4 6h16M4 12h16m-7 6h7'}
			></path>
		</svg>
	</button>

	<!-- Navigation Links (Desktop) -->
	<ul class="hidden space-x-6 lg:flex">
		{#each tabs as tab}
			<li>
				<button
					on:click={() => ($pageTabs = tab.name)}
					class="border-b-2 text-black transition-all
            {$pageTabs === tab.name
						? 'border-[#D12F2B] text-[#D12F2B]'
						: 'border-transparent text-[#D12F2B] hover:border-[#D12F2B] hover:text-[#D12F2B]'}"
				>
					{tab.label}
				</button>
			</li>
		{/each}
	</ul>

	<!-- Sign In Button (Desktop) -->
	<div class="hidden lg:block">
		<a href="https://www.veent.io/login/">
			<button
				class="rounded-full bg-[#D12F2B] px-8 py-2 text-lg font-bold text-white transition hover:bg-[#990C08]"
			>
				Sign In
			</button>
		</a>
	</div>
</nav>

<!-- Mobile Menu Dropdown -->
<ul
	class="{isOpen
		? 'block'
		: 'hidden'} absolute left-0 top-16 w-full space-y-4 bg-white p-4 shadow-lg lg:hidden"
>
	{#each tabs as tab}
		<li>
			<button
				on:click={() => (($pageTabs = tab.name), (isOpen = false))}
				class="block w-full border-b-2 py-2 text-left text-black transition-all
          {$pageTabs === tab.name
					? 'border-[#D12F2B] text-[#D12F2B]'
					: 'border-transparent text-[#D12F2B] hover:border-[#D12F2B] hover:text-[#D12F2B]'}"
			>
				{tab.label}
			</button>
		</li>
	{/each}

	<li>
		<a href="https://www.veent.io/login/">
			<button
				class="w-full rounded-full bg-[#D12F2B] px-8 py-2 text-lg font-bold text-white transition hover:bg-[#990C08]"
			>
				Sign In
			</button>
		</a>
	</li>
</ul>
