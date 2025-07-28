<script>
	import ProjectCard from '$lib/components/ProjectCard.svelte';

	const projects = [
		{
			title: 'Portfolio Website',
			description: 'A personal site built with SvelteKit and Tailwind.',
			github: '#',
			demo: '#'
		},
		{
			title: 'Todo App',
			description: 'A slick todo app with Svelte stores and localStorage.',
			github: '#',
			demo: '#'
		},
		{
			title: 'API Dashboard',
			description: 'A dashboard UI built for monitoring APIs and logs.',
			github: '#',
			demo: '#'
		}
	];
</script>

<section class="mx-auto max-w-6xl px-4 py-20">
	<h2 class="mb-12 text-center text-3xl font-bold">Projects</h2>
	<div class="grid gap-8 md:grid-cols-3">
		{#each projects as project}
			<ProjectCard {project} />
		{/each}
	</div>
</section>
