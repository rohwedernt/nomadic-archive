<script lang="ts">
	import '../app.css';
	import Header from './Header.svelte';
	import homeImage from '$lib/images/background-eli-mozjpeg.jpg';
	import aboutImage from '$lib/images/background-all.jpg';

	export let data: { url: URL };

	const backgrounds: Record<string, string> = {
		'/': homeImage,
		'/about': aboutImage
	};

	const backgroundAlts: Record<string, string> = {
		'/': 'Background image (Eli)',
		'/about': 'Background image (band)'
	};

	$: backgroundImage = backgrounds[data.url.pathname];
	$: backgroundAlt = backgroundAlts[data.url.pathname] || 'Background';
</script>

<a href="#main-content" class="visually-hidden skip-link">Skip to main content</a>

<div class="app">
	{#if backgroundImage}
		<img class="fullscreen-bg" src={backgroundImage} alt={backgroundAlt} />
	{/if}

	<Header />

	<main id="main-content">
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
		object-position: right top;
		pointer-events: none;

		@media (max-width: 640px) {
			object-position: center calc(-15px);
		}
	}

	.skip-link:focus {
		position: absolute;
		top: 0.5rem;
		left: 0.5rem;
		background: #fff;
		color: #111;
		padding: 0.5em 1em;
		border-radius: 0.5em;
		box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
		z-index: 10000;
		outline: 2px solid #0f28f3;
		clip: auto;
		width: auto;
		height: auto;
		white-space: normal;
	}
</style>
