<script lang="ts">
	import '../app.css';
	import Header from './Header.svelte';
	import homeImage from '$lib/images/background-eli.png';
	import aboutImage from '$lib/images/background-all.jpg';

	export let data: { url: URL };

	const backgrounds: Record<string, string> = {
		'/': homeImage,
		'/about': aboutImage
	};

	$: backgroundImage = backgrounds[data.url.pathname];
</script>

<div class="app">
	{#if backgroundImage}
		<img class="fullscreen-bg" src={backgroundImage} alt="Background" />
	{/if}

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
		object-position: right top;
		pointer-events: none;

		@media (max-width: 640px) {
			object-position: center top;
		}
	}
</style>
