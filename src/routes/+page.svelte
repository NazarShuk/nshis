<script lang="ts">
	import WavyText from '$lib/WavyText.svelte';

	const projects = [
		{
			name: 'Quizar',
			description: 'Quizlet clone that is completely free. Made because quizlet annoys me.',
			link: 'https://github.com/NazarShuk/quizar-rewrite'
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
		},
		{
			name: 'Ncord',
			description: 'A simple Discord clone i made for school.',
			link: 'https://ncord.vercel.app/'
		},
		{
			name: 'Quoter bot',
			description: 'A discord bot that generates an image for a quote.',
			link: 'https://github.com/NazarShuk/quoter'
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

<div class="flex h-screen w-full flex-col items-center justify-center text-center">
	<WavyText text="NshIS" class="text-8xl" />

	<p class="">
		hi my name is nazar, i'm a self-taught developer.
		<br />
		i mostly code in typescript, gdscript, and csharp.
	</p>
</div>

<div class="flex w-full flex-col items-center justify-center">
	<WavyText text="Projects" class="text-8xl" />

	<div class="mt-5 flex w-fit flex-col items-center justify-center gap-5">
		{#each projects as project (project.name)}
			<div
				class="w-full flex-1 flex-col items-center justify-center gap-2 rounded bg-neutral-100 p-2.5 transition dark:border-1 dark:border-neutral-800 dark:bg-neutral-900 dark:hover:border-neutral-700"
			>
				<a target="_blank" href={project.link}>
					<h2 class="text-xl font-bold">{project.name}</h2>
					<p>{project.description}</p>
				</a>
			</div>
		{/each}
	</div>
</div>

<div class="mt-20 flex w-full flex-col items-center justify-center">
	<WavyText text="Socials" class="text-8xl" />

	<div class="mt-5 flex w-full flex-row items-center justify-center gap-5">
		{#each socials as social (social.name)}
			<a target="_blank" href={social.link} class="flex flex-col items-center justify-center gap-2">
				<h2 class="text-xl font-bold {social.color}">{social.name}</h2>
			</a>
		{/each}
	</div>
</div>

<footer class="h-32"></footer>

<svelte:head>
	<title>NshIS</title>
</svelte:head>
