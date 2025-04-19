<script lang="ts">
		import BackgroundImage from '$lib/components/BackgroundImage.svelte';
		import backgroundImage from '$lib/images/background-eli.png';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="The Nomadic Archive" />
</svelte:head>

<BackgroundImage src={backgroundImage} />

<main>
	<div class="paper-panel">
		<div class="paper-content">
			<h1 class="text-2xl mb-4">🔎 Featured Finds 🔎</h1>
	
			<ul class="finds-list">
				<li class="text-lg pb-1">– 📸 This is where we'll 
					<a href="https://getemoji.com/" target="_blank" rel="noopener noreferrer">link</a>
				</li>
				<li class="text-lg pb-1">– 🎶 Some of the cool
					<a href="https://getemoji.com/" target="_blank" rel="noopener noreferrer">things</a>
				</li>
				<li class="text-lg pb-1">– 🔊 We find as we
					<a href="https://getemoji.com/" target="_blank" rel="noopener noreferrer">search for</a>
				</li>
				<li class="text-lg pb-1">– 🎶 
					<a href="https://getemoji.com/" target="_blank" rel="noopener noreferrer">More and more</a> Nomadic gems
				</li>
				<li class="text-lg pb-1">– 📹 To highlight
					<a href="https://getemoji.com/" target="_blank" rel="noopener noreferrer">them</a>
				</li>
				<li class="text-lg pb-1">– 📸 On the home page here for  
					<a href="https://getemoji.com/" target="_blank" rel="noopener noreferrer">viewing</a>
				</li>
				<li class="text-lg pb-1">– 📸 And for now I'm just using this test
					<a href="https://getemoji.com/" target="_blank" rel="noopener noreferrer">text</a>
				</li>
				<li class="text-lg pb-1">– 🔊 To see how this will look once there is   
					<a href="https://getemoji.com/" target="_blank" rel="noopener noreferrer">content</a>
				</li>
				<li class="text-lg pb-1">– 🔊 This is also a test
					<a href="https://getemoji.com/" target="_blank" rel="noopener noreferrer">link</a>
				</li>
				<li class="text-lg pb-1">– 📹 And actually I need one  
					<a href="https://getemoji.com/" target="_blank" rel="noopener noreferrer">more here</a>
				</li>
			</ul>
		</div>
	</div>
</main>

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
		overflow-y: auto;
		z-index: 2;
	}

	.paper-content {
		max-width: 90vw;
		margin: 0 auto;
		color: #111;
	}

	.finds-list {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: 0rem 4rem;
		list-style: none;
		padding: 0;
	}

	.finds-list li {
		font-size: 1.1rem;
	}

	@media (max-width: 640px) {
		.finds-list {
			grid-template-columns: 1fr;
		}
	}
</style>
