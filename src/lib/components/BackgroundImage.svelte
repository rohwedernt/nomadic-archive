<script lang="ts">
	export let src: string;
</script>

<img class="fullscreen-bg" {src} alt="Background" />

<style>
	.fullscreen-bg {
		position: fixed;
		top: 0;
		left: 0;
		width: 100vw;
		height: 100vh;
		z-index: -1;
		object-fit: cover;
		object-position: right top;
	}
</style>
