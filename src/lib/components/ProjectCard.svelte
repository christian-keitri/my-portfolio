<script>
	export let project;
</script>

<div class="rounded-lg bg-white p-6 shadow">
	<h3 class="mb-2 text-xl font-semibold">{project.title}</h3>
	<p class="mb-4 text-gray-700">{project.description}</p>
	<div class="flex gap-4">
		<a href={project.github} class="text-indigo-600 hover:underline">GitHub</a>
		<a href={project.demo} class="text-indigo-600 hover:underline">Live Demo</a>
	</div>
</div>
