<script lang="ts">
	import { onMount } from 'svelte';
	import { goto } from '$app/navigation';
	import CirclesRight from '$lib/circles-right.svelte';
	import Navigation from './navigation.svelte';
	import Aboutusblob from '../icons/aboutusblob.svelte';

	// let circles:any = [];

	// onMount(() => {
	//     circles = [
	//         { id: 1, size: '20px', color: 'bg-red-500', left: '62%', top: '29%', delay: '0s' },
	//         { id: 2, size: '15px', color: 'bg-rose-200', left: '55%', top: '48%', delay: '1s' },
	//         { id: 3, size: '25px', color: 'bg-amber-400', left: '64%', top: '64%', delay: '2s' }
	//     ];
	// });
</script>

<!-- <style>
  @keyframes float {
      0%, 100% { transform: translateY(0); opacity: 0.9; }
      50% { transform: translateY(-15px); opacity: 1; }
  }

  @keyframes rotateBlob {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}


  .floating-circle {
      position: absolute;
      border-radius: 50%;
      animation: float 3s ease-in-out infinite;
  }

  .blob {
  position: fixed;
  right: 0;
  top: 5%;
  margin-left: 30px;
  width: 40%;
  height: 80%;
  background-size: cover;
  background-position: center;
  clip-path: url(#cloudBlob);
  animation: rotateBlob 10s infinite linear;
}

     /* Keep Get Started Button Fully Visible */
     .get-started-btn {
      position: absolute;
      top: 10px;
      right: 20px;
      background-color: red; /* Ensure solid background */
      color: white;
      padding: 10px 20px;
      border-radius: 20px;
      font-weight: bold;
      z-index: 20; /* Higher than the blob */
  }
</style> -->
<CirclesRight />
<div
	class="relative h-screen min-h-screen w-full bg-[url('/ic')] bg-cover bg-center text-gray-900 sm:bg-contain md:bg-cover"
>
	<Navigation />

	<!-- Floating Circles -->
	<!-- {#each circles as circle}
      <div class="floating-circle {circle.color}"
          style="width: {circle.size}; height: {circle.size}; 
                 left: {circle.left}; top: {circle.top}; 
                 animation-delay: {circle.delay};">
                 
      </div>
  {/each}
  <svg width="0" height="0">
      <defs>
          <clipPath id="cloudBlob" clipPathUnits="objectBoundingBox">
              <path d="M0.3,0.9C-0.1,0.6,-0.1,0.3,0.2,0.2C0.1,-0.1,0.5,-0.1,0.6,0.1C0.8,0,1,0.2,1,0.4C1,0.6,0.9,0.8,0.7,0.9C0.6,1,0.4,1,0.3,0.9Z" />
          </clipPath>
      </defs>
  </svg> -->

	<!-- Blob Container -->
	<div class="blob"></div>
	<!-- Get Started Button -->
	<div class="fade-up m-[40px] min-h-screen text-gray-900">
		<section class="relative m-0 flex flex-col items-center px-12 md:flex-row">
			<!-- Left Content -->
			<div class=" relative space-y-6">
				<h3 class="text-lg font-bold text-red-500">About Veent</h3>
				<h2 class="text-5xl font-extrabold text-gray-900">Who are we?</h2>
				<p class="text-lg leading-relaxed text-gray-700">
					Veent was born from a simple idea: event registration shouldn’t be a headache. We believe
					anyone should be able to create and manage events with ease, regardless of technical
					expertise or budget.
				</p>
				<div class="space-y-6">
					<div>
						<h3 class="text-2xl font-bold text-red-500">Our Mission</h3>
						<p class="text-lg text-gray-700">
							To empower individuals and organizations to host unforgettable events through a
							user-friendly and affordable event management platform.
						</p>
					</div>
					<div>
						<h3 class="text-2xl font-bold text-orange-500">Our Vision</h3>
						<p class="text-lg text-gray-700">
							To become the leading all-in-one event management solution, simplifying the process
							for organizers of all backgrounds and budgets, and fostering a thriving community of
							event creators.
						</p>
					</div>
				</div>
				<Aboutusblob />

				<!-- Floating Action Button with Fixed Position -->
				<a
					href="/aboutus2"
					class=" bottom-8 left-8 flex h-12 w-12 cursor-pointer items-center justify-center rounded-full
bg-red-500 shadow-lg transition-transform hover:scale-110 hover:animate-bounce"
				>
					<span class="text-xl text-white">&#10132;</span>
				</a>
			</div>
		</section>
	</div>
</div>
