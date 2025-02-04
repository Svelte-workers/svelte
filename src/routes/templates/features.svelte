<script>
    const features = [
      { title: "Effortless", subtitle: "Event Pages" },
      { title: "Seamless", subtitle: "Payments" },
      { title: "Smart", subtitle: "Attendee Data" },
      { title: "Streamlined", subtitle: "Attendance" },
      { title: "Data-Driven", subtitle: "Decisions" },
    ];
  </script>
  
  <style>
    @import url('https://fonts.googleapis.com/css2?family=SF+Pro+Display:wght@400;700&display=swap');
    
    /* .feature {
      @apply bg-gradient-to-r from-pink-300 to-orange-300 rounded-full p-6 shadow-lg;
    } */
    .text-font {
      font-family: 'SF Pro Display', sans-serif;
    }
  </style>
  
  <div class="text-center p-10 bg-gradient-to-b from-pink-50 to-orange-50 min-h-screen">
    <h2 class="text-red-500 font-bold text-3xl text-font">Features</h2>
    <h1 class=" text-[30px] font-bold mt-2 text-font">Veent goes beyond basic registration.</h1>
    <p class="text-gray-600 mt-2 text-font">Our suite of features empowers you to create seamless event experiences. Choose a feature to see details.</p>
    
    <div class="grid grid-cols-2 md:grid-cols-3 gap-8 mt-10 max-w-4xl mx-auto">
      {#each features as feature}
        <div class="feature text-center">
          <h3 class="font-bold text-lg">{feature.title}</h3>
          <p class="text-sm text-gray-700">{feature.subtitle}</p>
        </div>
      {/each}
    </div>
  </div>
