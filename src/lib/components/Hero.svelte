<script lang="ts">
	const name = 'Against All Odds';
	const tagline = 'Where technology meets mission.';
	const sub = "Crossing borders and building tools — here's what I'm working on.";
</script>

<section class="min-h-screen flex flex-col justify-center px-6" style="background-color: #fafaf9">
	<div class="max-w-6xl mx-auto w-full pt-28 pb-20">

		<p class="text-sm font-semibold tracking-widest text-[#78716c] uppercase mb-6 animate-fade-up">
			Field Data · Missions · Technology
		</p>

		<h1 class="font-display text-7xl md:text-9xl font-semibold leading-none tracking-tight text-[#1c1917] mb-8 animate-fade-up delay-1">
			{name}
		</h1>

		<div class="w-32 h-1 rounded-full mb-8 animate-fade-up delay-2" style="background: linear-gradient(90deg, #f97316, #0ea5e9, #8b5cf6)"></div>

		<p class="text-sm text-[#78716c] italic mb-6 animate-fade-up delay-2">
			"Christ Jesus came into the world to save sinners — of whom I am the worst." — 1 Timothy 1:15–17
		</p>

		<p class="text-2xl md:text-3xl text-[#1c1917] font-light leading-snug mb-4 animate-fade-up delay-2">
			{tagline}
		</p>

		<p class="max-w-lg text-base text-[#78716c] leading-relaxed mb-12 animate-fade-up delay-3">
			{sub}
		</p>

		<div class="flex flex-wrap gap-4 animate-fade-up delay-4">
			<a
				href="#blog"
				class="inline-flex items-center gap-2 px-7 py-3.5 rounded-full bg-[#1c1917] text-[#fafaf9] font-semibold text-sm hover:opacity-75 transition-opacity duration-200"
			>
				Explore my work
				<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
					<path d="M12 5v14M5 12l7 7 7-7"/>
				</svg>
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
