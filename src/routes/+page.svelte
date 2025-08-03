<svelte:head>
	<title>The Nomadic Archives</title>
	<meta name="description" content="The Nomadic Archives" />
</svelte:head>

<main>
	<div class="paper-panel">
		<div class="paper-content">
			<h1 class="mb-4 text-2xl">🔎 Featured Finds</h1>

			<ul class="finds-list">
				<li class="pb-1">
					– 🔊 This spicy
					<a
						href="https://archive.org/details/nomadic2014-08-29/nomadic2014-08-2903.flac"
						target="_blank"
						rel="noopener noreferrer">Triple Wide</a
					>
					from Mantrabash '14 ft. Evan Bost or the INCREDIBLY fire
					<a
						href="https://archive.org/details/nomadic2014-08-29/nomadic2014-08-2906.flac"
						target="_blank"
						rel="noopener noreferrer">QAR</a
					>
					from that show or the only surviving recording of
					<a
						href="https://archive.org/details/nomadic2014-08-29/nomadic2014-08-2904.flac"
						target="_blank"
						rel="noopener noreferrer">Ghosts</a
					>
					(actually just go listen to that
					<a
						href="https://archive.org/details/nomadic2014-08-29"
						target="_blank"
						rel="noopener noreferrer">whole set</a
					>)
				</li>
				<li class="pb-1">
					– 🔗 The super old 
					<a href="https://rohwedernt.wixsite.com/nomadic" target="_blank" rel="noopener noreferrer"
						>Wix site</a
					> which is somehow still live
				</li>
				<li class="pb-1">
					– 📹 The vibes in this section of
					<a
						href="https://youtu.be/SJ-65jw5E3A?feature=shared"
						target="_blank"
						rel="noopener noreferrer">Daft Mother</a
					> from Boone in Blossom '15
				</li>
				<li class="pb-1">
					– 📹 What appears to be the only surviving audio of
					<a
						href="https://youtu.be/lqJbZSQ8yqg?feature=shared"
						target="_blank"
						rel="noopener noreferrer">Cable Jubilee</a
					>
				</li>
				<li class="pb-1">
					– 🔊 This
					<a
						href="https://archive.org/details/nm2014-02-15.nm2014-02-15sbd/03TripleWide.flac"
						target="_blank"
						rel="noopener noreferrer">Triple Wide</a
					> from Martin's Downtown in Roanoke ft. Keith Allen
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
		padding: 2rem;
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

	.finds-list {
		column-count: 2;
		column-gap: 4rem;
		list-style: none;
		padding: 0;
	}

	.finds-list li {
		font-size: 0.9rem;
	}

	@media (max-width: 640px) {
		.finds-list {
			grid-template-columns: 1fr;
			column-count: 1;
		}
	}
</style>
