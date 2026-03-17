<script lang="ts">
	import '../app.css';
	import Nav from '$lib/components/Nav.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import ParallaxBackground from '$lib/components/ParallaxBackground.svelte';

	let { children } = $props();
</script>

<ParallaxBackground />

<div class="site-content">
	<Nav />
	<main>
		{@render children()}
	</main>
	<Footer />
</div>

<style>
	.site-content {
		position: relative;
		z-index: 1;
	}
</style>
