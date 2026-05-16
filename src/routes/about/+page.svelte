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
			Nomadic lived during a magical chaotic blur in the early 2010s. Over time, the media trail we
			left behind scattered across the internet like birdshot — Facebook posts, Instagram accounts
			we can't log into, maybe a rogue Myspace link, definitely a ReverbNation page (…is that still
			a thing?), and a Dropbox folder that hasn't been cracked open since the Obama years.
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
		max-height: 55vh;
		background: rgb(248, 242, 224);
		border-top: 2px solid #9a8060;
		padding: 1.25rem 2rem;
		overflow-y: scroll;
		z-index: 2;
	}

	.paper-content {
		max-width: 90vw;
		margin: 0 auto;
		color: #1a1a1a;
		font-family: 'Courier New', Courier, monospace;
	}

	.paper-content h1 {
		font-size: 0.85rem;
		font-weight: 700;
		letter-spacing: 0.2em;
		text-transform: uppercase;
		border-bottom: 1px solid #b5a080;
		padding-bottom: 0.4rem;
		margin-bottom: 0.75rem;
	}
</style>
