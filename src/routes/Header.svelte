<script lang="ts">
	import { page } from '$app/state';
	import titleMobile from '$lib/images/title-mobile.png';
	import titleTablet from '$lib/images/title-tablet.png';
	import titleFull from '$lib/images/title-full.png';
</script>

<header>
	<nav>
		<ul>
			<li aria-current={page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Home</a>
			</li>
			<li aria-current={page.url.pathname === '/about' ? 'page' : undefined}>
				<a href="/about">About</a>
			</li>
			<li aria-current={page.url.pathname.startsWith('/archive') ? 'page' : undefined}>
				<a href="/archive">Archive</a>
			</li>
		</ul>
	</nav>

	<!-- Responsive title image -->
	<picture class="title-banner">
		<source srcset={titleFull} media="(min-width: 800px)" />
		<source srcset={titleTablet} media="(min-width: 640px)" />
		<img src={titleMobile} alt="Nomadic Title" />
	</picture>
</header>

<style>
	header {
		display: flex;
		justify-content: center;
	}

	.title-banner {
		position: absolute;
		top: 0;
		left: 0;
		width: 100vw;
		display: block;
		z-index: -1;
	}

	.title-banner img {
		width: 90%;
		height: auto;
		display: block;
		@media (max-width: 480px) {
			padding-top: 1rem;
			margin: auto;
		}
	}

	nav {
		background: rgba(242, 239, 230, 0.93);
		clip-path: polygon(0% 0%, 100% 0%, calc(100% - 2em) 100%, 2em 100%);
		padding: 0 2.5em;
		z-index: 999;
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
	}

	li {
		position: relative;
		height: 100%;
	}

	li[aria-current='page']::before {
		--size: 10px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid #5a3010;
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 1rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: #5a3010;
	}
</style>
