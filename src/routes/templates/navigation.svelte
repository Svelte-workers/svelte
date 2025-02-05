<script>
  import { pageTabs } from "../../stores/userVariables";
  let isOpen = false;

  const tabs = [
    { name: "home", label: "Home" },
    { name: "aboutUs", label: "About Us" },
    { name: "features", label: "Features" },
    { name: "pricing", label: "Pricing" },
    { name: "contactUs", label: "Kontaka dri" }
  ];
</script>

<nav class="mx-6 p-4 flex items-center justify-between">
  <!-- Logo -->
  <div>
    <img class="w-24" src="/veent-logo.svg" alt="veent">
  </div>

  <!-- Mobile Menu Button -->
  <button class="lg:hidden block text-black focus:outline-none" on:click={() => isOpen = !isOpen}>
    <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="{isOpen ? 'M6 18L18 6M6 6l12 12' : 'M4 6h16M4 12h16m-7 6h7'}"></path>
    </svg>
  </button>

  <!-- Navigation Links (Desktop) -->
  <ul class="hidden lg:flex space-x-6">
    {#each tabs as tab}
      <li>
        <button 
          on:click={() => ($pageTabs = tab.name)} 
          class="text-black border-b-2 transition-all 
            {($pageTabs === tab.name) 
              ? 'text-[#D12F2B] border-[#D12F2B]' 
              : 'border-transparent text-[#D12F2B] hover:border-[#D12F2B] hover:text-[#D12F2B]'}">
          {tab.label}
        </button>
      </li>
    {/each}
  </ul>

  <!-- Sign In Button (Desktop) -->
  <div class="hidden lg:block">
    <a href="https://www.veent.io/login/">
      <button class="bg-[#D12F2B] font-bold text-white text-lg py-2 px-8 rounded-lg hover:bg-[#990C08] transition">
        Sign In
      </button>
    </a>
  </div>
</nav>

<!-- Mobile Menu Dropdown -->
<ul class="{isOpen ? 'block' : 'hidden'} lg:hidden bg-white absolute top-16 left-0 w-full shadow-lg p-4 space-y-4">
  {#each tabs as tab}
    <li>
      <button 
        on:click={() => ($pageTabs = tab.name, isOpen = false)} 
        class="block w-full text-left text-black border-b-2 transition-all py-2 
          {($pageTabs === tab.name) 
            ? 'text-[#D12F2B] border-[#D12F2B]' 
            : 'border-transparent text-[#D12F2B] hover:border-[#D12F2B] hover:text-[#D12F2B]'}">
        {tab.label}
      </button>
    </li>
  {/each}
  
  <li>
    <a href="https://www.veent.io/login/">
      <button class="bg-[#D12F2B] font-bold text-white text-lg py-2 px-8 w-full rounded-lg hover:bg-[#990C08] transition">
        Sign In
      </button>
    </a>
  </li>
</ul>
