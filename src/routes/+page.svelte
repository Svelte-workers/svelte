<script lang="ts">
	import { pageTabs } from "../stores/userVariables";
	import AboutUs from "./templates/aboutUs.svelte";
	import Features from "./templates/features.svelte";
	import ContactUs from "./templates/contactUs.svelte";
	import HomePage from "./templates/homePage.svelte";
	import Navigation from "./templates/navigation.svelte";

	import Pricing from "./templates/pricing.svelte";
  $pageTabs = "home";
</script>
<Navigation/>

{#if $pageTabs=="home"}
    <HomePage/>
{:else if $pageTabs == "aboutUs"}
    <AboutUs/>
{:else if $pageTabs == "features"}
    <Features/>
{:else if $pageTabs == "pricing"}
    <Pricing/>
{:else if $pageTabs == "contactUs"}
    <ContactUs/>
{/if}  