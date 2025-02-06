<script lang="ts">
    import Navigation from './navigation.svelte';
    import CustomizedAboutusCircle from '$lib/customized-aboutus-circle.svelte';
	import { pageTabs } from '../../stores/userVariables';
  </script>
  
  <div class="relative min-h-screen bg-gradient-to-r from-white via-pink-50 to-white">
    <!-- Navigation Bar -->
    <Navigation />
    <div class="relative md:w-1/3">
        <img
          src="/path/to/your/image.png"
          alt="Event audience"
          class="rounded-2xl shadow-lg object-cover"
        />
      </div>
    <!-- Main Content Section -->
    <div class="py-16 px-8 md:px-20 fade-up">
      <section class="flex flex-col md:flex-row-reverse items-center gap-12">
        <!-- Right Content -->
         
        <div class="space-y-8 relative md:w-2/3">
          <h3 class="text-xl font-bold text-red-500">About Veent</h3>
          <h2 class="text-5xl font-extrabold text-gray-900">What we do?</h2>
          <p class="w-[80%] text-lg text-gray-700 leading-relaxed">
            <span class="font-bold">Veent</span> is a powerful yet delightfully simple web app that streamlines the entire event registration process. From creating captivating event pages to managing RSVPs and attendee information, <span class="font-bold">Veent</span> takes care of the heavy lifting, allowing you to focus on what matters most – making your event a success.
          </p>
          
          <div>
            <h3 class="text-2xl font-bold text-orange-500">The Veent Team</h3>
            <p class="w-[80%] text-lg text-gray-700 leading-relaxed">
              Veent is a passionate group of individuals dedicated to building innovative solutions for event organizers. We come from diverse backgrounds, but we share a common goal: to make event management a breeze for everyone.
            </p>
          </div>
          <CustomizedAboutusCircle/>
          <!-- Navigation Buttons -->
          <div class="flex items-center space-x-4">
            <!-- Previous Button -->
            <a 
              role="button" 
              on:click={() => pageTabs.set("aboutUs")} 
              class="w-12 h-12 bg-red-500 rounded-full flex items-center justify-center 
                     shadow-lg cursor-pointer hover:scale-110 hover:animate-bounce transition-transform"
            >
            <span class="text-white text-xl" style="transform: rotate(180deg);">&#10132;</span>
        </a>
            <!-- Next Button -->

            <a 
              role="button" 
              on:click={() => pageTabs.set("aboutUs3")} 
              class="w-12 h-12 bg-red-500 rounded-full flex items-center justify-center 
                     shadow-lg cursor-pointer hover:scale-110 hover:animate-bounce transition-transform"
            >
              <span class="text-white text-xl">&#10132;</span>
            </a>
          </div>
          
        </div>
      </section>
    </div>
  
    <!-- Decorative Blob -->
    <div class="absolute top-[-100px] left-[-150px] w-[500px] h-[500px] bg-gradient-to-r from-pink-300 via-red-300 to-orange-300 
                rounded-full opacity-30 z-[-1]"></div>
  </div>
  