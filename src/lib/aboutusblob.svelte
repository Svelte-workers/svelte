<script lang="ts">

</script>
<div>
  <svg  viewBox="0 0 600 600" width="500" height="500" style="overflow: visible;">
    <g style="transform-origin: 60% 50%; animation: rotate-clip 50s linear infinite;">
      <defs>
        <clipPath id="blob-clip">
          <path 
        
            d="M 77.0 212.5 A 135.5 135.5 0 1 1 348.0 212.5 A 135.5 135.5 0 1 1 77.0 212.5
               M 322.0 334.0 A 86.0 86.0 0 1 1 494.0 334.0 A 86.0 86.0 0 1 1 322.0 334.0
               M 250.0 96.0 A 56.0 56.0 0 1 1 362.0 96.0 A 56.0 56.0 0 1 1 250.0 96.0
               M 77.0 358.5 A 126.5 126.5 0 1 1 330.0 358.5 A 126.5 126.5 0 1 1 77.0 358.5
               M 293.0 449.0 A 111.0 111.0 0 1 1 515.0 449.0 A 111.0 111.0 0 1 1 293.0 449.0
               M 252.0 227.5 A 131.5 131.5 0 1 1 515.0 227.5 A 131.5 131.5 0 1 1 252.0 227.5
               M 191.0 463.5 A 65.5 65.5 0 1 1 322.0 463.5 A 65.5 65.5 0 1 1 191.0 463.5"
          />
        </clipPath>
      </defs>
      <image 
        x="0" 
        y="0" 
        width="600" 
        height="600" 
        href="https://i.ibb.co/mCgkr07M/image.png" 
        clip-path="url(#blob-clip)"
      />
    </g>
  </svg>
  
</div>
<style>
  @keyframes rotate-clip {
    from {
      transform: rotate(10deg);
    }
    to {
      transform: rotate(360deg);
    }
  }

  svg path {
    transform-origin: 60% 50%; /* Center of rotation */
    animation: rotate-clip 50s linear infinite; /* Slow spin */
  
  }
</style>