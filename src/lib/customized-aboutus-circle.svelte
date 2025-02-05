<script lang="ts">
    // Array of circle properties (position, size, color, animation duration, animation delay)
    const circleRight = [
        { top: "15%", right: "5%", size: "40px", color: "linear-gradient(135deg, #FFB2B0, #D45B58)", duration: "20s", delay: "0.5s" },
        { top: "40%", right: "10%", size: "20px", color: "linear-gradient(135deg, #F3CCCF, #E0A6A6)", duration: "20s", delay: "0.5s" },
        { top: "60%", right: "65%", size: "35px", color: "linear-gradient(135deg, #EDD2AE, #EAA23F)", duration: "20s", delay: "0.5s" }
    ];
</script>

<style>
  @keyframes float {
      0%, 100% { transform: translate(0, 0); opacity: 0.9; }
      25% { transform: translate(-10px, -20px); opacity: 1; }
      50% { transform: translate(10px, 0px); }
      75% { transform: translate(-10px, 20px); }
  }

  .floating-circle {
      position: absolute;
      border-radius: 50%;
      animation: float ease-in-out infinite;
  }
</style>

<!-- Floating Circles -->
{#each circleRight as circle}
    <div
        class="floating-circle"
        style="top: {circle.top}; left: {circle.right}; width: {circle.size}; height: {circle.size}; background: {circle.color}; animation-duration: {circle.duration}; animation-delay: {circle.delay};"
    ></div>
{/each}

<slot></slot>