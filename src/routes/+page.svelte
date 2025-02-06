<script lang="ts">
	import { pageTabs } from '../stores/userVariables';
	import AboutUs from './templates/aboutUs.svelte';
	import AboutUs2 from './templates/aboutUs2.svelte';
	import AboutUs3 from './templates/aboutUs3.svelte';
	import Features from './templates/features.svelte';
	import ContactUs from './templates/contactUs.svelte';
	import HomePage from './templates/homePage.svelte';
	import Navigation from './templates/navigation.svelte';
	import Pricing from './templates/pricing.svelte';
	import Effortless from './templates/effortless.svelte';
	import Smart from './templates/smart.svelte';
	import Seamless from './templates/seamless.svelte';
	import Stream from './templates/stream.svelte';
	import DataDriven from './templates/data_driven.svelte';
	$pageTabs = 'home';
</script>



{#if $pageTabs == 'home'}
	<HomePage />
{:else if $pageTabs == 'aboutUs'}
	<AboutUs/>
{:else if $pageTabs == 'aboutUs2'}
	<AboutUs2/>
{:else if $pageTabs == 'aboutUs3'}
	<AboutUs3/>
{:else if $pageTabs == 'features'}
	<Features />
{:else if $pageTabs == 'pricing'}
	<Pricing />
{:else if $pageTabs == 'contactUs'}
	<ContactUs />
{:else if $pageTabs == 'effortless'}
	<Effortless />
{:else if $pageTabs == 'smart'}
	<Smart />
{:else if $pageTabs == 'seamless'}
	<Seamless />
{:else if $pageTabs == 'stream'}
	<Stream />
{:else if $pageTabs == 'data_driven'}
	<DataDriven />
{/if}
