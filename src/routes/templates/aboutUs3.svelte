<script lang=ts>
  import AboutusCircle from '$lib/aboutus-circle.svelte';
  import Navigation from './navigation.svelte';
  import { pageTabs } from '../../stores/userVariables';
  
</script>
<div class="background relative min-h-screen text-gray-900">
    
  <Navigation/>
<!-- Blob Container -->
 
<div class="blob"></div>

  <!-- Get Started Button -->
<div class="m-[30px] fade-up  text-gray-900">
    
    <section class="relative flex flex-col md:flex-row-reverse items-center px-12 m-0">
        <!-- Right Content -->
        <div class="relative md:w-1/3">
            <img
              src="/path/to/your/image.png"
              alt="Event audience"
              class="rounded-2xl shadow-lg object-cover"
            />
          </div>
 
      <div class=" space-y-8 relative">
          <h3 class="text-[23px] text-red-500 font-bold ">About Veent</h3>
          <h2 class="text-5xl font-extrabold text-gray-900">Who are we?</h2>
          <p class="w-[70%] text-lg text-gray-700 leading-relaxed">
              Veent was born from a simple idea: event registration shouldn’t be a headache.
              We believe anyone should be able to create and manage events with ease,
              regardless of technical expertise or budget.
          </p>
          <div class="space-y-6">
              <div>
                  <h3 class="text-2xl font-bold text-red-700">Our Mission</h3>
                  <p class=" w-[70%] text-lg text-gray-700">To empower individuals and organizations to host unforgettable events through a user-friendly and affordable event management platform.</p>
              </div>
              <div>
                  <h3 class="text-2xl font-bold text-orange-500">Our Vision</h3>
                  <p class="w-[70%] text-lg text-gray-700">To become the leading all-in-one event management solution, simplifying the process for organizers of all backgrounds and budgets, and fostering a thriving community of event creators.</p>
              </div>
          </div>
          <AboutusCircle/>

<!-- Floating Action Button with Fixed Position -->
<a 
role="button" 
on:click={() => pageTabs.set("aboutUs2")} 
class="w-12 h-12 bg-red-500 rounded-full flex items-center justify-center 
       shadow-lg cursor-pointer hover:scale-110 hover:animate-bounce transition-transform"
>
<span class="text-white text-xl" style="transform: rotate(180deg);">&#10132;</span>
</a>
      </div>
  </section>
</div>
</div>