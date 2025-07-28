<script lang="ts">
	import '../app.css';
	import Footer from '../components/Footer.svelte';
	import Header from '../components/Header.svelte';

	let y = 0;
	let innerHeight = 0;
	let innerWidth = 0;

	function goTop() {
		document.body.scrollIntoView({ behavior: 'smooth' });
	}
</script>

<div class="relative mx-auto flex min-h-screen w-full max-w-[1400px] flex-col text-sm sm:text-base">
	<!-- Back to top button -->
	<div
		class={'fixed bottom-0 z-[10] flex w-full p-10 duration-200 ' +
			(y > 0 ? 'pointer-events-auto opacity-100' : 'pointer-events-none opacity-0')}
	>
		<button
			on:click={goTop}
			class="ml-auto aspect-square cursor-pointer rounded-full bg-slate-900 px-3 text-violet-400 hover:bg-slate-800 sm:px-4"
		>
			<i class="fa-solid fa-arrow-up grid aspect-square place-items-center"></i>
			<span class="sr-only">Scroll to top</span>
		</button>
	</div>

	<Header {y} />
	<slot />
	<Footer />
</div>

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />
