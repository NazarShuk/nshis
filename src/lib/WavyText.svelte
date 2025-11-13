<script lang="ts">
	let props: { text: string; class?: string } = $props();
</script>

<h1 class={props.class}>
	{#each props.text.split('') as letter, i (i)}
		<span class="animate-wavy relative inline-block" style="animation-delay: {i * 0.5}s">
			{letter}
		</span>
	{/each}
</h1>
