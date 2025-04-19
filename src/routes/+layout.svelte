<script lang="ts">
	import '../app.css';
	import Header from './Header.svelte';
	import homeImage from '$lib/images/background-eli.png';
	import aboutImage from '$lib/images/background-greg.jpg';
	import archivesImage from '$lib/images/background-all.jpg';
	import defaultImage from '$lib/images/background-eli.png';

	export let data: { url: URL };

	const backgrounds: Record<string, string> = {
		'/': homeImage,
		'/about': aboutImage,
		'/archives': archivesImage
	};

	$: backgroundImage = backgrounds[data.url.pathname] ?? defaultImage;
</script>

<div class="app">
	<img class="fullscreen-bg" src={backgroundImage} alt="Background" />

	<Header />

	<main>
		<slot />
	</main>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	.fullscreen-bg {
		position: fixed;
		top: 0;
		left: 0;
		width: 100vw;
		height: 100vh;
		z-index: -1;
		object-fit: cover;
		object-position: left top;
		pointer-events: none;
	}
</style>
