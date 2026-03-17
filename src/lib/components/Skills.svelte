<script lang="ts">
	const categories = [
		{
			name: 'Design',
			items: ['Figma', 'Canva', 'UI/UX', 'Branding', 'Typography']
		},
		{
			name: 'Frontend',
			items: ['Svelte', 'TypeScript', 'HTML/CSS', 'Tailwind', 'React']
		},
		{
			name: 'Backend & Tools',
			items: ['Node.js', 'Git', 'GitHub Actions', 'REST APIs']
		}
	];
</script>

<section id="skills" class="py-32 px-6">
	<div class="max-w-6xl mx-auto">

		<div class="mb-16">
			<p class="text-sm font-medium tracking-widest text-[--color-accent] uppercase mb-4">Expertise</p>
			<h2 class="font-display text-4xl md:text-5xl font-semibold text-[--color-text] leading-tight">
				Tools & skills
			</h2>
		</div>

		<div class="grid md:grid-cols-3 gap-10">
			{#each categories as { name, items }}
				<div>
					<h3 class="text-xs font-semibold tracking-widest uppercase text-[--color-muted] mb-5">
						{name}
					</h3>
					<div class="flex flex-wrap gap-2.5">
						{#each items as skill}
							<span class="px-3.5 py-2 rounded-lg border border-[--color-border] text-sm text-[--color-text] bg-[--color-surface] hover:border-[--color-accent]/50 hover:text-[--color-accent] transition-all duration-200 cursor-default">
								{skill}
							</span>
						{/each}
					</div>
				</div>
			{/each}
		</div>

	</div>
</section>
