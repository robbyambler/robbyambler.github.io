<script lang="ts">
	const name = 'Robby Ambler';
	const tagline = 'Where technology meets mission.';
	const sub = "I've spent my career building systems and crossing borders — because the right tools in the right hands can change what's possible.";
</script>

<section class="relative min-h-screen flex flex-col justify-center px-6">
	<div class="max-w-5xl mx-auto w-full pt-28 pb-20">

		<!-- Eyebrow -->
		<p class="text-sm font-medium tracking-widest text-[--color-accent] uppercase mb-7 animate-fade-up">
			Field Data · Missions · Technology
		</p>

		<!-- Name -->
		<h1 class="font-display text-6xl md:text-8xl font-semibold leading-none tracking-tight text-[--color-text] mb-8 animate-fade-up delay-1">
			{name}
		</h1>

		<!-- Tagline -->
		<p class="text-2xl md:text-3xl text-[--color-muted] font-light leading-snug mb-6 animate-fade-up delay-2">
			{tagline}
		</p>

		<!-- Sub -->
		<p class="max-w-lg text-base text-[--color-muted] leading-relaxed mb-12 animate-fade-up delay-3">
			{sub}
		</p>

		<!-- CTAs -->
		<div class="flex flex-wrap gap-4 animate-fade-up delay-4">
			<a
				href="#about"
				class="inline-flex items-center gap-2 px-7 py-3.5 rounded-full bg-[--color-accent] text-[#070e1a] font-semibold text-sm hover:opacity-90 transition-opacity duration-200"
			>
				My story
			</a>
		</div>
	</div>
</section>

<style>
	@keyframes fadeUp {
		from { opacity: 0; transform: translateY(18px); }
		to   { opacity: 1; transform: translateY(0); }
	}
	:global(.animate-fade-up)  { animation: fadeUp 0.7s ease forwards; }
	:global(.delay-1) { animation-delay: 0.1s;  opacity: 0; }
	:global(.delay-2) { animation-delay: 0.22s; opacity: 0; }
	:global(.delay-3) { animation-delay: 0.34s; opacity: 0; }
	:global(.delay-4) { animation-delay: 0.46s; opacity: 0; }
</style>
