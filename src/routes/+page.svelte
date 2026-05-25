<script lang="ts">
	import Hero from '$lib/components/Hero.svelte';
	import ProjectSection from '$lib/components/ProjectSection.svelte';
</script>

<svelte:head>
	<title>Against All Odds</title>
</svelte:head>

<Hero />

<ProjectSection
	id="blog"
	num="01"
	eyebrow="Writing & Reflection"
	title="Blog"
	description="Sermons, devotions, and field notes — a personal record of faith, mission, and the questions worth sitting with."
	cta="Read the blog"
	href="#"
	accent="#f97316"
	bg="#fff7ed"
/>

<ProjectSection
	id="phases"
	num="02"
	eyebrow="MCP Server"
	title="Phases of Engagement"
	description="A structured framework for understanding the arc of missionary work — from first contact to sustainable partnership."
	cta="Explore the tool"
	href="#"
	accent="#0ea5e9"
	bg="#f0f9ff"
	flip={true}
/>

<ProjectSection
	id="mdcu"
	num="03"
	eyebrow="Fan Theory"
	title="Matt Damon Cinematic Universe"
	description="A tongue-in-cheek but internally consistent theory: every Matt Damon character is the same person. One arc, eighteen aliases, and a friend from South Boston who knew him before any of it started."
	cta="Enter the MDCU"
	href="https://robbyambler.github.io/MDCU/mdcu.html"
	repoHref="https://github.com/robbyambler/MDCU/"
	accent="#8b5cf6"
	bg="#f5f3ff"
/>
