<script lang="ts">
	interface Props {
		id: string;
		num: string;
		eyebrow: string;
		title: string;
		description: string;
		cta: string;
		href: string;
		accent: string;
		bg: string;
		flip?: boolean;
	}

	let { id, num, eyebrow, title, description, cta, href, accent, bg, flip = false }: Props = $props();
</script>

<section {id} class="min-h-screen flex items-center px-6 py-24" style="background-color: {bg}">
	<div class="max-w-6xl mx-auto w-full">
		<div class="grid md:grid-cols-2 gap-16 items-center {flip ? 'md:[&>*:first-child]:order-2 md:[&>*:last-child]:order-1' : ''}">

			<div>
				<p class="text-xs font-semibold tracking-widest uppercase mb-5" style="color: {accent}">
					{eyebrow}
				</p>
				<h2 class="font-display text-5xl md:text-6xl font-semibold leading-tight text-[#1c1917] mb-6">
					{title}
				</h2>
				<p class="text-lg text-[#78716c] leading-relaxed mb-10 max-w-md">
					{description}
				</p>
				<a
					href={href}
					target="_blank"
					rel="noopener noreferrer"
					class="inline-flex items-center gap-2 px-7 py-3.5 rounded-full text-white font-semibold text-sm transition-opacity hover:opacity-80"
					style="background-color: {accent}"
				>
					{cta}
					<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
						<path d="M7 17L17 7M17 7H7M17 7v10"/>
					</svg>
				</a>
			</div>

			<div class="hidden md:flex items-center justify-center overflow-hidden">
				<span
					class="font-display font-bold select-none leading-none"
					style="font-size: 22rem; color: {accent}; opacity: 0.08; line-height: 0.85"
				>{num}</span>
			</div>

		</div>
	</div>
</section>
