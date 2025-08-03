<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="paper-panel">
	<div class="paper-content">
		<h1 class="mb-2 text-2xl">🎛️ About This Site</h1>

		<p class="pb-2 text-sm">
			<b>Welcome to The Nomadic Archives</b> — a dusty digital attic packed with photos, videos, poorly
			recorded live sets, show-poster masterpieces, and whatever other fragments we thought had been
			lost to the void.
		</p>
		<p class="pb-2 text-sm">
			Nomadic lived during a magical chaotic blur in the early 2010s. Over time, the media
			trail we left behind scattered across the internet like birdshot — Facebook posts, Instagram
			accounts we can't log into, maybe a rogue Myspace link, definitely a ReverbNation page (…is
			that still a thing?), and a Dropbox folder that hasn't been cracked open since the Obama
			years.
		</p>
		<p class="text-sm">
			This site is our attempt to gather all that chaos into one place — a living, breathing Nomadic
			vault. A permanent, safely stored, redundantly backed-up home for all of it.
		</p>
	</div>
</div>

<style>
	.paper-panel {
		position: fixed;
		bottom: 0;
		left: 0;
		width: 100%;
		height: 30vh;
		background: rgba(255, 255, 255, 0.75);
		backdrop-filter: blur(8px);
		-webkit-backdrop-filter: blur(8px);
		border-top-left-radius: 1rem;
		border-top-right-radius: 1rem;
		box-shadow: 0 -8px 30px rgba(0, 0, 0, 0.15);
		padding: 1.5rem;
		overflow-y: scroll;
		z-index: 2;

		@media (max-width: 640px) {
			height: 35vh;
		}
	}

	.paper-content {
		max-width: 90vw;
		margin: 0 auto;
		color: #111;
	}
</style>
