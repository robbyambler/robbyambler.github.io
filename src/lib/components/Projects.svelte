<script lang="ts">
	interface Project {
		title: string;
		description: string;
		tags: string[];
		href?: string;
		githubHref?: string;
		featured?: boolean;
	}

	const projects: Project[] = [
		{
			title: 'GAPP',
			description: 'A field reporting and progress-tracking system built for missionaries working among unreached peoples. Designed to make complex data simple enough to use in the field — and meaningful enough to inform strategy at scale.',
			tags: ['Field Data', 'Missions', 'Web App'],
			href: 'https://taethni.com/GAPP',
			featured: true
		}
	];
</script>

<section id="projects" class="py-32 px-6 bg-[--color-surface-alpha]">
	<div class="max-w-5xl mx-auto">

		<div class="flex items-end justify-between mb-16">
			<div>
				<p class="text-sm font-medium tracking-widest text-[--color-accent] uppercase mb-4">Work</p>
				<h2 class="font-display text-4xl md:text-5xl font-semibold text-[--color-text] leading-tight">
					Selected projects
				</h2>
			</div>
			<a
				href="https://github.com/robbyambler"
				target="_blank"
				rel="noopener"
				class="hidden md:inline-flex items-center gap-2 text-sm text-[--color-muted] hover:text-[--color-text] transition-colors"
			>
				View all on GitHub
				<svg width="14" height="14" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
					<path stroke-linecap="round" stroke-linejoin="round" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"/>
				</svg>
			</a>
		</div>

		<div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6 max-w-sm md:max-w-none">
			{#each projects as project}
				<article
					class="group relative flex flex-col p-7 rounded-2xl border border-[--color-border] bg-[--color-surface-2] hover:border-[--color-accent]/40 transition-all duration-300"
					class:featured={project.featured}
				>
					{#if project.featured}
						<span class="absolute top-4 right-4 text-xs font-medium tracking-widest uppercase text-[--color-accent] bg-[--color-accent]/10 px-2.5 py-1 rounded-full">
							Featured
						</span>
					{/if}

					<h3 class="text-lg font-semibold text-[--color-text] mb-3 group-hover:text-[--color-accent] transition-colors">
						{project.title}
					</h3>
					<p class="text-sm text-[--color-muted] leading-relaxed flex-1 mb-6">
						{project.description}
					</p>

					<!-- Tags -->
					<div class="flex flex-wrap gap-2 mb-6">
						{#each project.tags as tag}
							<span class="text-xs px-2.5 py-1 rounded-full border border-[--color-border] text-[--color-muted]">
								{tag}
							</span>
						{/each}
					</div>

					<!-- Links -->
					<div class="flex items-center gap-4">
						{#if project.href}
							<a href={project.href} target="_blank" rel="noopener"
								class="text-xs font-medium text-[--color-text] hover:text-[--color-accent] transition-colors flex items-center gap-1.5">
								Visit site
								<svg width="12" height="12" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
									<path stroke-linecap="round" stroke-linejoin="round" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"/>
								</svg>
							</a>
						{/if}
						{#if project.githubHref}
							<a href={project.githubHref} target="_blank" rel="noopener"
								class="text-xs font-medium text-[--color-muted] hover:text-[--color-text] transition-colors flex items-center gap-1.5">
								GitHub
								<svg width="12" height="12" viewBox="0 0 24 24" fill="currentColor">
									<path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"/>
								</svg>
							</a>
						{/if}
					</div>
				</article>
			{/each}
		</div>
	</div>
</section>
