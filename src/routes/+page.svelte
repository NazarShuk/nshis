<script lang="ts">
	const projects = [
		{
			name: 'Ncord',
			description: 'A simple Discord clone i made for school.',
			link: 'https://ncord.vercel.app/'
		},
		{
			name: 'Quoter bot',
			description: 'A discord bot that generates an image for a quote.',
			link: 'https://github.com/NazarShuk/quoter'
		},
		{
			name: 'Quizar',
			description: 'Quizlet clone that is completely free. Made because quizlet annoys me.',
			link: 'https://github.com/NazarShuk/quizar'
		},
		{
			name: 'Schedule',
			description: 'A simple website that shows time left until the end of class',
			link: 'https://github.com/NazarShuk/schedule-app'
		},
		{
			name: 'Epic fight sim',
			description: 'Parody of those "x vs y" tiktoks using AI',
			link: 'https://github.com/NazarShuk/epic-fight-sim'
		},
		{
			name: 'IXL Solver',
			description: 'App that uses AI to solve IXL questions',
			link: 'https://github.com/NazarShuk/IXL-solver'
		}
	];

	const socials = [
		{
			name: 'Github',
			link: 'https://github.com/NazarShuk',
			color: 'text-gray-500'
		},
		{
			name: 'YouTube',
			link: 'https://youtube.com/@nshis',
			color: 'text-red-500'
		}
	];
</script>

<div class="flex h-screen w-full flex-col items-center justify-center font-sans">
	<h1 class="mb-5 text-8xl font-bold">
		{#each 'NshIS'.split('') as letter, i (i)}
			<span class="animate-wavy relative inline-block" style="animation-delay: {i * 0.2}s">
				{letter}
			</span>
		{/each}
	</h1>
	<h2>i make websites and stuff</h2>
</div>

<div class="flex w-full flex-col items-center justify-center font-sans">
	<h1 class="animate-stretch-and-wiggle mb-5 text-8xl font-bold">
		{#each 'Projects'.split('') as letter, i (i)}
			<span class="animate-wavy relative inline-block" style="animation-delay: {i * 0.2}s">
				{letter}
			</span>
		{/each}
	</h1>

	<div class="mt-5 flex w-full flex-col items-center justify-center gap-5">
		{#each projects as project (project.name)}
			<a
				target="_blank"
				href={project.link}
				class="flex w-full flex-col items-center justify-center gap-2"
			>
				<h2 class="text-3xl font-bold">{project.name}</h2>
				<p class="text-xl">{project.description}</p>
			</a>
		{/each}
	</div>
</div>

<div class="mt-20 flex w-full flex-col items-center justify-center font-sans">
	<h1 class="animate-stretch-and-wiggle mb-5 text-8xl font-bold">
		{#each 'Socials'.split('') as letter, i (i)}
			<span class="animate-wavy relative inline-block" style="animation-delay: {i * 0.2}s">
				{letter}
			</span>
		{/each}
	</h1>

	<div class="mt-5 flex w-full flex-row items-center justify-center gap-5">
		{#each socials as social (social.name)}
			<a target="_blank" href={social.link} class="flex flex-col items-center justify-center gap-2">
				<h2 class="text-3xl font-bold {social.color}">{social.name}</h2>
			</a>
		{/each}
	</div>
</div>

<footer class="h-32"></footer>

<svelte:head>
	<title>NshIS</title>
</svelte:head>
