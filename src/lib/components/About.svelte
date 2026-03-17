<script lang="ts">
	const highlights = [
		{ label: 'Based in', value: 'Henrico, VA' }
	];
</script>

<section id="about" class="py-32 px-6">
	<div class="max-w-5xl mx-auto">

		<div class="grid md:grid-cols-[1fr_1.6fr] gap-16 items-start">

			<!-- Left -->
			<div>
				<p class="text-sm font-medium tracking-widest text-[--color-accent] uppercase mb-4">About</p>
				<h2 class="font-display text-4xl md:text-5xl font-semibold text-[--color-text] leading-tight mb-10">
					Two worlds.<br/>One calling.
				</h2>

				<!-- Quick facts -->
				<div class="flex flex-col gap-5">
					{#each highlights as { label, value }}
						<div class="flex items-center gap-4">
							<span class="text-xs tracking-widest uppercase text-[--color-muted] w-24 shrink-0">{label}</span>
							<span class="h-px flex-1 bg-[--color-border]"></span>
							<span class="text-sm text-[--color-text] text-right">{value}</span>
						</div>
					{/each}
				</div>

				<!-- Warm accent quote -->
				<blockquote class="mt-12 pl-4 border-l-2 border-[--color-warm] text-[--color-muted] text-sm leading-relaxed italic">
					"…a great multitude that no one could count, from every nation, tribe, people and language."
					<span class="block mt-2 not-italic text-xs tracking-wide text-[--color-warm]">Revelation 7:9</span>
				</blockquote>
			</div>

			<!-- Right: bio -->
			<div class="space-y-6 text-[--color-muted] leading-relaxed text-[0.97rem]">
				<p>
					I started in academic technology — managing systems, training faculty, supporting the infrastructure that keeps institutions running. Good, useful work. But in 2012 I stepped away from that to serve as a career missionary overseas, and spent over a decade on the ground leading teams, building partnerships, and working among people in places most of the world has never thought about. Somewhere in the middle of all that, I found myself building data systems and tracking tools for our teams — and realizing that the technology wasn't separate from the mission. It was part of it.
				</p>
				<p>
					That's the thread the Lord keeps revealing. He brought me back from overseas with a heart to do the same work, even among the same peoples, but with a renewed focus on getting solid tools and technology into the hands of those at the ends of the earth. Today I manage systems and support tools that missionaries around the world rely on to understand where the work is going — and where it still needs to go.
				</p>
			</div>

		</div>
	</div>
</section>
