<script lang="ts">
	let scrollY = $state(0);

	$effect(() => {
		const onScroll = () => { scrollY = window.scrollY; };
		window.addEventListener('scroll', onScroll, { passive: true });
		return () => window.removeEventListener('scroll', onScroll);
	});

	// Each blob moves at its own rate — layered depth effect
	const b1y = $derived(scrollY * 0.18);
	const b2y = $derived(scrollY * 0.09);
	const b3y = $derived(scrollY * 0.25);
	const b4y = $derived(scrollY * 0.12);
</script>

<!-- Fixed full-screen layer, sits behind everything -->
<div class="parallax-bg" aria-hidden="true">

	<!-- Subtle grid -->
	<div class="grid-overlay"></div>

	<!-- Blobs -->
	<div class="blob blob-1" style="transform: translateY({b1y}px)"></div>
	<div class="blob blob-2" style="transform: translateY({b2y}px)"></div>
	<div class="blob blob-3" style="transform: translateY({b3y}px)"></div>
	<div class="blob blob-4" style="transform: translateY({b4y}px)"></div>
</div>

<style>
	.parallax-bg {
		position: fixed;
		inset: 0;
		z-index: 0;
		overflow: hidden;
		pointer-events: none;
	}

	.grid-overlay {
		position: absolute;
		inset: 0;
		background-image:
			linear-gradient(to right, rgba(255,255,255,0.016) 1px, transparent 1px),
			linear-gradient(to bottom, rgba(255,255,255,0.016) 1px, transparent 1px);
		background-size: 72px 72px;
	}

	.blob {
		position: absolute;
		border-radius: 50%;
		filter: blur(100px);
		will-change: transform;
	}

	/* Top-left — large sky blue anchor */
	.blob-1 {
		width: 800px; height: 800px;
		background: radial-gradient(circle, #0ea5e9 0%, transparent 65%);
		opacity: 0.12;
		top: -200px; left: -200px;
	}

	/* Bottom-right — mid sky blue */
	.blob-2 {
		width: 500px; height: 500px;
		background: radial-gradient(circle, #38bdf8 0%, transparent 65%);
		opacity: 0.10;
		bottom: 5%; right: -100px;
	}

	/* Mid-page — warm gold glint, very faint */
	.blob-3 {
		width: 350px; height: 350px;
		background: radial-gradient(circle, #fbbf24 0%, transparent 65%);
		opacity: 0.055;
		top: 55%; left: 40%;
	}

	/* Upper-right — deeper blue depth layer */
	.blob-4 {
		width: 450px; height: 450px;
		background: radial-gradient(circle, #0369a1 0%, transparent 65%);
		opacity: 0.13;
		top: 10%; right: 10%;
	}
</style>
