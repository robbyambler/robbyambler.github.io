<script lang="ts">
	let scrolled = $state(false);

	$effect(() => {
		const onScroll = () => { scrolled = window.scrollY > 20; };
		window.addEventListener('scroll', onScroll, { passive: true });
		return () => window.removeEventListener('scroll', onScroll);
	});

	const links = [
		{ href: '#blog',   label: 'Blog',           color: '#f97316' },
		{ href: '#phases', label: 'Phases',          color: '#0ea5e9' },
		{ href: '#mdcu',   label: 'Matt Damon CU',  color: '#8b5cf6' },
	];
</script>

<nav
	class="fixed top-0 left-0 right-0 z-50 transition-all duration-300"
	class:scrolled
>
	<div class="max-w-6xl mx-auto px-6 py-4 flex items-center justify-between">
		<a href="/" class="font-display text-lg font-semibold tracking-tight text-[#1c1917] hover:opacity-60 transition-opacity">
			AAO
		</a>

		<div class="hidden md:flex items-center gap-8">
			{#each links as { href, label, color }}
				<a
					{href}
					class="nav-link text-sm text-[#78716c] hover:text-[#1c1917] transition-colors duration-200"
					style="--link-color: {color}"
				>
					{label}
				</a>
			{/each}
		</div>

		<a
			href="mailto:robby.ambler@gmail.com"
			class="hidden md:inline-flex items-center gap-2 px-4 py-2 rounded-full text-sm font-medium border border-[#e7e5e4] text-[#1c1917] hover:bg-[#f5f5f4] transition-all duration-200"
		>
			Get in touch
		</a>
	</div>
</nav>

<style>
	nav.scrolled {
		background-color: rgba(250, 250, 249, 0.92);
		backdrop-filter: blur(14px);
		border-bottom: 1px solid #e7e5e4;
	}

	.nav-link {
		text-decoration: none;
		text-underline-offset: 4px;
		text-decoration-thickness: 1.5px;
	}

	.nav-link:hover {
		text-decoration: underline;
		text-decoration-color: var(--link-color);
	}
</style>
