<script lang="ts">
	import Hero from '$lib/components/Hero.svelte';
	import ProjectSection from '$lib/components/ProjectSection.svelte';
</script>

<svelte:head>
	<title>Against All Odds</title>
</svelte:head>

<Hero />

<ProjectSection
	id="oikos"
	num="01"
	eyebrow="Web App"
	title="Oikos Map"
	description="Map the people in your household of influence: who you're praying for, sharing the gospel with, and equipping to do the same. Squares are believers, circles are not yet. Everything stays in your own browser."
	cta="Build your map"
	href="https://robbyambler.github.io/Oikos-map/"
	repoHref="https://github.com/robbyambler/Oikos-map/"
	accent="#10b981"
	bg="#ecfdf5"
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

<ProjectSection
	id="nab"
	num="04"
	eyebrow="Network"
	title="North American Bengali Network"
	description="Uniting practitioners across North America who are committed to reaching Bengali communities with the gospel."
	cta="Visit the network"
	href="https://nabnetwork.org"
	accent="#f59e0b"
	bg="#fffbeb"
	flip={true}
/>

<ProjectSection
	id="reachrva"
	num="05"
	eyebrow="Gospel Advance Strategy"
	title="Reach RVA"
	description="A comprehensive gospel advance and church planting strategy for the Richmond, VA metro area. No place left without a gospel witness."
	cta="Explore the strategy"
	href="https://reachrva.com"
	accent="#e11d48"
	bg="#fff1f2"
/>
