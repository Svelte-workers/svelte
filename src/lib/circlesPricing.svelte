<script lang="ts">
	// Array of circle properties (position, size, color, animation duration, animation delay)
	const circleLeft = [
		{
			top: '15%',
			left: '20%',
			size: '20px',
			color: 'linear-gradient(135deg, #FFB2B0, #D45B58)',
			duration: '6s',
			delay: '0s'
		},
		{
			top: '25%',
			left: '13%',
			size: '15px',
			color: 'linear-gradient(135deg, #F3CCCF, #E0A6A6)',
			duration: '7s',
			delay: '0.5s'
		},
		{
			top: '35%',
			left: '15%',
			size: '25px',
			color: 'linear-gradient(135deg, #EDD2AE, #EAA23F)',
			duration: '8s',
			delay: '1s'
		},
		{
			top: '65%',
			left: '15%',
			size: '20px',
			color: 'linear-gradient(135deg, #EDD2AE, #EAA23F)',
			duration: '6s',
			delay: '0s'
		},
		{
			top: '75%',
			left: '13%',
			size: '15px',
			color: 'linear-gradient(135deg, #F3CCCF, #E0A6A6)',
			duration: '7s',
			delay: '0.5s'
		},
		{
			top: '85%',
			left: '20%',
			size: '25px',
			color: 'linear-gradient(135deg, #FFB2B0, #D45B58)',
			duration: '8s',
			delay: '1s'
		},

		{
			top: '15%',
			left: '80%', // Moved to the right
			size: '20px',
			color: 'linear-gradient(135deg, #FFB2B0, #D45B58)',
			duration: '6s',
			delay: '0s'
		},
		{
			top: '25%',
			left: '87%', // Moved to the right
			size: '15px',
			color: 'linear-gradient(135deg, #F3CCCF, #E0A6A6)',
			duration: '7s',
			delay: '0.5s'
		},
		{
			top: '35%',
			left: '85%', // Moved to the right
			size: '25px',
			color: 'linear-gradient(135deg, #EDD2AE, #EAA23F)',
			duration: '8s',
			delay: '1s'
		},
		{
			top: '65%',
			left: '85%', // Moved to the right
			size: '20px',
			color: 'linear-gradient(135deg, #EDD2AE, #EAA23F)',
			duration: '6s',
			delay: '0s'
		},
		{
			top: '75%',
			left: '87%', // Moved to the right
			size: '15px',
			color: 'linear-gradient(135deg, #F3CCCF, #E0A6A6)',
			duration: '7s',
			delay: '0.5s'
		},
		{
			top: '85%',
			left: '80%', // Moved to the right
			size: '25px',
			color: 'linear-gradient(135deg, #FFB2B0, #D45B58)',
			duration: '8s',
			delay: '1s'
		}
	];
</script>

<!-- Floating Circles -->
{#each circleLeft as circle}
	<div
		class="floating-circle"
		style="top: {circle.top}; left: {circle.left}; width: {circle.size}; height: {circle.size}; background: {circle.color}; animation-duration: {circle.duration}; animation-delay: {circle.delay};"
	></div>
{/each}

<slot></slot>

<style>
	@keyframes float {
		0%,
		100% {
			transform: translate(0, 0);
			opacity: 0.9;
		}
		25% {
			transform: translate(-10px, -20px);
			opacity: 1;
		}
		50% {
			transform: translate(10px, 0px);
		}
		75% {
			transform: translate(-10px, 20px);
		}
	}

	.floating-circle {
		position: absolute;
		border-radius: 50%;
		animation: float ease-in-out infinite;
	}
</style>
