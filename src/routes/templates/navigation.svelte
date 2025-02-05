<script>
  import { pageTabs } from "../../stores/userVariables";
  const tabs = [{name:"home",label:"Home"},
             {name:"aboutUs",label:"About Us"},
             {name:"features",label:"Features"},
             {name:"pricing",label:"Pricing"},
             {name:"contactUs",label:"Kontaka dri"}];
//   const tabs = ["home",
//              "aboutUs",
//              "features",
//              "pricing",
//              "contactUs"];
</script>

<nav class="mx-[60px] p-4 flex items-center justify-between">
  <div>
      <img class="w-[6rem]" src="/veent-logo.svg" alt="veent">
  </div>

  <ul class="flex space-x-4">
      {#each tabs as tab}
          <li>
              <button 
                  on:click={() => ($pageTabs = tab.name)} 
                  class="mx-[30px] pt-[8px] text-black border-b-[3px] transition-all 
                    {($pageTabs === tab.name) 
                      ? 'text-[#D12F2B] border-[#D12F2B]' 
                      : 'border-transparent text-[#D12F2B] hover:border-[#D12F2B] hover:text-[#D12F2B]'}">

                  {tab.label}
              </button>
          </li>
      {/each}
  </ul>

  <div>

    <a href="https://www.veent.io/login/">
        <button class="bg-[#D12F2B] font-bold text-white text-[16px] py-2 px-[40px] rounded-[10px] hover:bg-[#990C08] transition">
          Sign In
      </button>
    </a>
      
  </div>
</nav>

