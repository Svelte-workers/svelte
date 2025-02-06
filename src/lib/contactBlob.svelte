<div class="blob">
	<svg
		viewBox="0 0 500 500"
		xmlns="http://www.w3.org/2000/svg"
		xmlns:xlink="http://www.w3.org/1999/xlink"
		width="100%"
		id="blobSvg"
	>
		<defs>
			<linearGradient id="gradient" x1="0%" y1="0%" x2="0%" y2="100%">
				<stop offset="0%" style="stop-color: rgb(245, 213, 212);"></stop>
				<stop offset="100%" style="stop-color: rgb(222, 109, 106);"></stop>
			</linearGradient>
		</defs>
		<path
			id="blob"
			d="M446.5,286Q461,322,448.5,358.5Q436,395,409.5,424Q383,453,335.5,426.5Q288,400,259,445Q230,490,203,454Q176,418,144.5,408.5Q113,399,80.5,379Q48,359,60,319.5Q72,280,69,249.5Q66,219,50,176Q34,133,62.5,105Q91,77,129.5,70Q168,63,202,72.5Q236,82,265,78.5Q294,75,335,65.5Q376,56,406.5,80.5Q437,105,446,142.5Q455,180,443.5,215Q432,250,446.5,286Z"
			fill="url(#gradient)"
		></path>
	</svg>
</div>

<style>
	.blob {
		--size: 600px; /* Increased size */
		position: absolute;
		width: 120%; /* Increase width */
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		transition: 3s all;
		animation:
			floating 4s ease-in-out infinite,
			scaling 3s ease-in-out infinite;
		z-index: -1; /* Moves blob behind ContactUs */
		opacity: 0.5; /* Optional: Reduce opacity */
	}

	.blob > svg {
		height: var(--size);
		width: var(--size);
		position: absolute;
		display: block;
		top: calc(50% - var(--size) / 2);
		transition: 1s all 0.13s ease-in-out;
		animation: rotate 30s linear infinite;
	}

	.blob > svg:first-child {
		left: calc(50% - var(--size) / 2);
	}

	.blob > svg:last-child {
		right: calc(50% - var(--size) / 2);
	}

	.blob > svg::before {
		content: '';
		display: block;
		opacity: 0.6;
		height: 100%;
		width: 100%;
		background-blend-mode: color;
		transition:
			2s all 0.25s ease-in-out,
			1.5s opacity,
			background-size 1.5s;
		animation: rotate 30s infinite linear both;

		mask:
			radial-gradient(circle, #000 50%, transparent 50%) 50% 50% / var(--size) var(--size),
			radial-gradient(circle, #000 50%, transparent 50%) 110% 10% / calc(var(--size) / 1.3)
				calc(var(--size) / 1.3),
			radial-gradient(circle, #000 50%, transparent 50%) -20% 20% / calc(var(--size) / 1.2)
				calc(var(--size) / 1.2),
			radial-gradient(circle, #000 50%, transparent 50%) 10% 110% / calc(var(--size) / 1.6)
				calc(var(--size) / 1.3);

		mask-repeat: no-repeat;
	}

	.blob > svg:last-child::before {
		animation-direction: reverse;
	}

	.blob > svg:first-child::before {
		background:
			radial-gradient(circle, #f5d5d4 50%, transparent 50%) 50% 50% / 0 0,
			linear-gradient(#f5d5d4, #de6d6a 40%) 50% 50% / 100% 100%;
		background-repeat: no-repeat;
	}

	.blob > svg:last-child::before {
		background:
			radial-gradient(circle, #de6d6a 50%, transparent 50%) 50% 50% / 0 0,
			linear-gradient(#f5d5d4, #de6d6a) 50% 50% / 100% 100%;
		background-repeat: no-repeat;
	}
	@keyframes rotate {
		0% {
			transform: rotate(0deg);
		}
		100% {
			transform: rotate(360deg);
		}
	}

	@keyframes scaling {
		0% {
			transform: translate(-50%, -50%) scale(1);
		}
		50% {
			transform: translate(-50%, -50%) scale(1.1);
		}
		100% {
			transform: translate(-50%, -50%) scale(1);
		}
	}
</style>
