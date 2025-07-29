<script>
	export let y;

	let tabs = [
		{ name: 'Projects', link: '#projects' },
		{ name: 'About me', link: '#about' }
	];
</script>

<header
	class={'sticky top-0 z-[10] flex items-center justify-between px-6 duration-200' +
		(y > 0 ? 'border-violet-950 bg-slate-950 py-4' : ' border-transparent bg-transparent py-6')}
>
	<h1 class="font-medium">
		<b class="poppins font-bold">Christian</b> BOB
	</h1>
	<div class="ml-auto hidden items-center gap-4 pr-4 sm:flex">
		{#each tabs as tab, index}
			<a href={tab.link} class="duration-200 hover:text-violet-400">
				<p>{tab.name}</p>
			</a>
		{/each}
	</div>

	<a
		href="https://github.com/christian-keitri"
		target="_blank"
		class="blueShadow group relative overflow-hidden rounded-full bg-white px-5 py-2 text-slate-950"
	>
		<div
			class="absolute top-0 right-full z-0 h-full w-full bg-violet-400 opacity-20 duration-200 group-hover:translate-x-full"
		></div>
		<h4>Get in touch</h4>
	</a>
</header>
