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
		repoHref?: string;
	}

	let { id, num, eyebrow, title, description, cta, href, accent, bg, flip = false, repoHref }: Props = $props();
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
				<div class="flex items-center gap-4 flex-wrap">
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

					{#if repoHref}
						<a
							href={repoHref}
							target="_blank"
							rel="noopener noreferrer"
							class="inline-flex items-center gap-2 text-sm font-medium text-[#78716c] hover:text-[#1c1917] transition-colors"
						>
							<svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor">
								<path d="M12 2C6.477 2 2 6.477 2 12c0 4.418 2.865 8.166 6.839 9.489.5.092.682-.217.682-.482 0-.237-.009-.868-.013-1.703-2.782.604-3.369-1.341-3.369-1.341-.454-1.154-1.11-1.462-1.11-1.462-.908-.62.069-.608.069-.608 1.003.07 1.531 1.03 1.531 1.03.892 1.529 2.341 1.087 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.647 0 0 .84-.269 2.75 1.025A9.578 9.578 0 0 1 12 6.836a9.59 9.59 0 0 1 2.504.337c1.909-1.294 2.747-1.025 2.747-1.025.546 1.377.203 2.394.1 2.647.64.699 1.028 1.592 1.028 2.683 0 3.842-2.339 4.687-4.566 4.935.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.741 0 .267.18.578.688.48C19.138 20.163 22 16.418 22 12c0-5.523-4.477-10-10-10z"/>
							</svg>
							View on GitHub
						</a>
					{/if}
				</div>
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
