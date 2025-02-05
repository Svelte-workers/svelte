<script>
	import { pageTabs } from '../../stores/userVariables';
	const tabs = [
		{ name: 'home', label: 'Home' },
		{ name: 'aboutUs', label: 'About Us' },
		{ name: 'features', label: 'Features' },
		{ name: 'pricing', label: 'Pricing' },
		{ name: 'contactUs', label: 'Contact Us' }
	];
	//   const tabs = ["home",
	//              "aboutUs",
	//              "features",
	//              "pricing",
	//              "contactUs"];
</script>

<nav
	class="sticky top-0 z-50 mt-[10px] flex items-center justify-between p-4 px-[90px] backdrop-blur-2xl
"
>
	<div>
		<img class="w-[6rem]" src="/veent-logo.svg" alt="veent" />
	</div>

	<ul class="flex space-x-4">
		{#each tabs as tab}
			<li>
				<button
					on:click={() => ($pageTabs = tab.name)}
					class="mx-[20px] border-b-[3px] pt-[8px] text-black transition-all
                    {$pageTabs === tab.name
						? 'border-[#D12F2B] text-[#D12F2B]'
						: 'border-transparent text-[#D12F2B] hover:border-[#D12F2B] hover:text-[#D12F2B]'}"
				>
					{tab.label}
				</button>
			</li>
		{/each}
	</ul>

	<div>
		<a href="https://www.veent.io/login/">
			<button
				class="rounded-[10px] bg-[#D12F2B] px-[40px] py-2 text-[16px] font-bold text-white transition hover:bg-[#990C08]"
			>
				Sign In
			</button>
		</a>
	</div>
</nav>
