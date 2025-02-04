<script>
	import Blob from "$lib/blob.svelte";
	import CirclesLeft from "$lib/circles-left.svelte";
	import CirclesRight from "$lib/circles-right.svelte";
    

</script>


<div class="">
    <CirclesLeft/>
</div>

<div class="">
    <CirclesRight />
</div>



<div class="flex items-center justify-center min-h-screen">
    <div class="fade-down text-center relative flex flex-col items-center justify-center">

       <!-- Blob Positioned Behind Everything -->
       <div class="absolute inset-0 flex justify-center items-center z-[-1]">
           <Blob />
       </div>
       
       <!-- Veent Image -->
       <img class="w-[350px] h-[120px] relative z-10" src="/veent.png" alt="veent">

       <!-- Main Text Content -->
       <div class="font-bold text-[28px] text-[#D12F2B] mt-2">
            Events, simplified.
       </div>
       <div class="w-[650px] text-center text-[20px] text-black mt-2">
            Streamline event registration with Veent. Our user-friendly web app makes creating events a breeze. Packed with features and affordable pricing, Veent simplifies event management for everyone.
       </div>
       
       <!-- Call-to-action Button -->
       <div class="my-[40px]">
        <a href="https://www.veent.io/signup">
            <button class="bg-[#D12F2B] font-bold text-white text-[16px] py-2 px-[40px] rounded-[10px] hover:bg-[#990C08] transition">
                Sign up for free!
             </button>
        </a>      
       </div>
    </div>
</div>
