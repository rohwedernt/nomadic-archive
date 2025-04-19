<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="paper-panel">
	<div class="paper-content h-full">
		<h1 class="mb-8 text-center text-4xl">🗄️ The Archives 🗄️</h1>
		<div class="flex items-center justify-center h-4/5 "><h1 class="text-lg text-slate-800">Coming Soon! 🥳</h1></div>
	</div>
</div>

<style>
	.paper-panel {
		position: fixed;
		bottom: 0;
		left: 0;
		width: 100%;
		height: 50vh;
		background: rgba(255, 255, 255, 0.85);
		backdrop-filter: blur(8px);
		-webkit-backdrop-filter: blur(8px);
		border-top-left-radius: 1rem;
		border-top-right-radius: 1rem;
		box-shadow: 0 -8px 30px rgba(0, 0, 0, 0.15);
		padding: 2rem;
		overflow-y: auto;
		z-index: 2;
	}

	.paper-content {
		max-width: 90vw;
		margin: 0 auto;
		color: #111;
	}
</style>
