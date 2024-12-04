<script>
	import { onMount } from 'svelte';
	import logo from '$lib/assets/D3.png';

	let logoElement;
	let containerElement;

	onMount(() => {
		const containerWidth = containerElement.clientWidth;
		const containerHeight = containerElement.clientHeight;
		const logoWidth = logoElement.clientWidth;
		const logoHeight = logoElement.clientHeight;

		let x = Math.random() * (containerWidth - logoWidth);
		let y = Math.random() * (containerHeight - logoHeight);
		let xSpeed = 2;
		let ySpeed = 2;

		function updatePosition() {
			x += xSpeed;
			y += ySpeed;

			if (x <= 0 || x >= containerWidth - logoWidth) {
				xSpeed = -xSpeed;
			}
			if (y <= 0 || y >= containerHeight - logoHeight) {
				ySpeed = -ySpeed;
			}

			logoElement.style.left = `${x}px`;
			logoElement.style.top = `${y}px`;

			requestAnimationFrame(updatePosition);
		}

		updatePosition();
	});
</script>

<div bind:this={containerElement} class="logo-container">
	<img bind:this={logoElement} src={logo} alt="" class="animated-logo" />
</div>

<style>
	.logo-container {
		margin: auto;
		position: relative;
		width: 100%;
		height: 400px; /* Set a fixed height for the container */
		overflow: hidden; /* Hide overflow to keep the logo within the container */
	}
	img {
		width: 200px; /* Set a fixed width for the logo */
		height: auto;
		position: absolute; /* Position the logo absolutely within the container */
	}
</style>
