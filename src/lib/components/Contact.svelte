<script lang="ts">
	const email = 'robby.ambler@gmail.com';
	const linkedin = 'https://www.linkedin.com/in/robby-ambler';
</script>

<section id="contact" class="py-32 px-6 bg-[--color-surface-alpha]">
	<div class="max-w-5xl mx-auto">

		<div class="max-w-2xl">
			<p class="text-sm font-medium tracking-widest text-[--color-accent] uppercase mb-4">Contact</p>
			<h2 class="font-display text-4xl md:text-5xl font-semibold text-[--color-text] leading-tight mb-6">
				Let's connect.
			</h2>
			<p class="text-[--color-muted] leading-relaxed mb-12">
				Whether it's a project, a question, or just a good conversation about technology and mission — I'd love to hear from you.
			</p>

			<div class="flex items-center gap-4">
				<a
					href="mailto:{email}"
					class="flex items-center justify-center w-12 h-12 rounded-full border border-[--color-border] text-[--color-muted] hover:border-[--color-accent] hover:text-[--color-accent] transition-all duration-200"
					aria-label="Email"
				>
					<svg width="20" height="20" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.75">
						<path stroke-linecap="round" stroke-linejoin="round" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
					</svg>
				</a>

				<a
					href={linkedin}
					target="_blank"
					rel="noopener"
					class="flex items-center justify-center w-12 h-12 rounded-full border border-[--color-border] text-[--color-muted] hover:border-[--color-accent] hover:text-[--color-accent] transition-all duration-200"
					aria-label="LinkedIn"
				>
					<svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
						<path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
					</svg>
				</a>
			</div>
		</div>
	</div>
</section>
