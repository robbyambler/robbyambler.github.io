<script lang="ts">
	let scrolled = $state(false);

	$effect(() => {
		const onScroll = () => { scrolled = window.scrollY > 20; };
		window.addEventListener('scroll', onScroll, { passive: true });
		return () => window.removeEventListener('scroll', onScroll);
	});

	const links = [
		{ href: '#about',   label: 'About' },
		{ href: '#contact', label: 'Contact' }
	];
</script>

<nav
	class="fixed top-0 left-0 right-0 z-50 transition-all duration-300"
	class:scrolled
>
	<div class="max-w-5xl mx-auto px-6 py-4 flex items-center justify-between">
		<a href="/" class="font-display text-lg font-semibold tracking-tight text-[--color-text] hover:text-[--color-accent] transition-colors">
			RA
		</a>

		<div class="hidden md:flex items-center gap-8">
			{#each links as { href, label }}
				<a
					{href}
					class="text-sm text-[--color-muted] hover:text-[--color-text] transition-colors duration-200"
				>
					{label}
				</a>
			{/each}
		</div>

		<a
			href="#contact"
			class="hidden md:inline-flex items-center gap-2 px-4 py-2 rounded-full text-sm font-medium border border-[--color-border] text-[--color-text] hover:border-[--color-accent] hover:text-[--color-accent] transition-all duration-200"
		>
			Let's talk
		</a>
	</div>
</nav>

<style>
	nav.scrolled {
		background-color: rgba(7, 14, 26, 0.88);
		backdrop-filter: blur(14px);
		border-bottom: 1px solid var(--color-border);
	}
</style>
