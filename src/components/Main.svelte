<script>
	import Step from './Step.svelte';
	let steps = [
		{
			name: 'SmolBob Store',
			icon: 'fa-solid fa-cart-shopping',
			href: 'https://github.com/christian-keitri/my-app'
		},
		{
			name: 'Habit Tracker',
			icon: 'fa-solid fa-list-check',
			href: 'https://github.com/christian-keitri/habit_tracker'
		},
		{
			name: 'Music App',
			icon: 'fa-solid fa-music',
			href: 'https://github.com/christian-keitri/music'
		}
	];

	let benefits = [
		{
			name: 'a self taught developer',
			description:
				'I taught myself to code using free online resources and absolutely fell in love with the creativity and problem solving that is involved in developing and engineering innovative new online experiences. Starting of with JavaScript, HTML & CSS and evolving my knowledge base to include JavaScript frameworks, backend programming, design, cloud services and much much more.'
		},
		{
			name: 'a product design & UX fanatic',
			description:
				'Carefully crafting and designing amazing user experiences allows me to express and experiment with every morsel of creativity I have. I love the challenge of learning new design concepts and enabling users with amazing online experiences.'
		},
		{
			name: 'an excellent communicator',
			description:
				"Communication is key and it's a paramount value of mine. I believe in transparency and constructive communication above all else. This helps me develop deep relationships and ensures my effectiveness and productivity in any work space with any team."
		}
	];

	function previewResume() {
		const fileUrl = '/downloads/SalapateCV.pdf';
		window.open(fileUrl, '_blank');
	}

	function downloadResume() {
		const fileUrl = '/downloads/SalapateCV.pdf';
		const link = document.createElement('a');
		link.href = fileUrl;
		link.download = 'SalapateCV.pdf';
		document.body.appendChild(link);
		link.click();
		document.body.removeChild(link);
	}
</script>

<main class="flex flex-1 flex-col p-4">
	<section id="introPage" class="grid grid-cols-1 gap-10 py-8 sm:py-14 lg:grid-cols-2">
		<div class="flex flex-col gap-6 text-center md:gap-8 lg:justify-center lg:gap-10 lg:text-left">
			<h2 class="mdtext-6xl text-4xl font-semibold sm:text-5xl">
				Hi! I'm <span class="poppins text-violet-400">Christian</span> BOB <br />Junior Web
				<span class="poppins text-violet-400">Developer</span>
			</h2>
			<p class="text-base sm:text-lg md:text-xl">
				My <span class="poppins text-violet-400"> favorite tech</span> includes JavaScript, Node.js,
				NestJS Svelte, Flutter, TailwindCss, PostgresSQL, Docker.
			</p>
			<a
				class="blueShadow poppins group relative mx-auto cursor-pointer overflow-hidden rounded-full bg-white px-6 py-3 text-base text-slate-950 sm:text-lg md:text-xl lg:mr-auto"
				href="https://www.facebook.com/christian.cj.768517/"
				target="_blank"
			>
				<div
					class="absolute top-0 right-full z-0 h-full w-full bg-violet-400 opacity-20 duration-200 group-hover:translate-x-full"
				></div>
				<h4>Get in touch &rarr;</h4>
			</a>
		</div>
		<div class="relative grid place-items-center shadow-2xl">
			<img
				src="/images/profile.png"
				alt=""
				role="presentation"
				class="z-[2] max-h-[70vh] rounded-full border-4 border-white object-cover"
			/>
		</div>
	</section>

	<section id="projects" class="flex flex-col gap-24 py-20 lg:py-32">
		<div class="flex flex-col gap-2 text-center">
			<h6 class="text-large sm:text-xl md:text-2xl">A few of my creative endeavors.</h6>
			<h3 class="text-3xl font-semibold sm:text-4xl md:text-5xl">
				Curious to <span class="poppins text-violet-400">see</span>my work?
			</h3>
		</div>
		<a
			href="https://www.facebook.com/christian.cj.768517"
			target="_blank"
			class="mx-auto -mt-10 -mb-4 flex items-center
             gap-2 rounded-md border border-solid border-white px-4 py-2
             duration-200 hover:border-violet-700 sm:-mb-0"
		>
			<i class="fa-regular fa-circle-play"></i>
			<p>Check my Featured Post</p>
		</a>
		<div class="grid grid-cols-1 gap-12 lg:grid-cols-3 lg:gap-10">
			<Step step={steps[0]}>
				<p>
					<strong class="text-violet-400">SmolBob Store</strong> is a modern e-commerce platform
					built using
					<strong class="text-violet-400">Flutter</strong>, designed to deliver a fast, smooth, and
					responsive shopping experience across both Android and iOS devices.
				</p>
			</Step>
			<Step step={steps[1]}>
				<p>
					<strong class="text-violet-400">The Habit Tracker</strong> is a Flutter-powered app that lets
					users track both good and bad habits, with features like reminders, notes, progress charts,
					and a clean, user-friendly interface.
				</p>
			</Step>
			<Step step={steps[2]}>
				<p>
					<strong class="text-violet-400">The Music App</strong> is a Spotify-style clone built with
					<strong class="text-violet-400">Flutter</strong> for the frontend and a custom Python backend
					for streaming and user management.
				</p>
			</Step>
		</div>
	</section>

	<section
		id="about"
		class="relative flex flex-col gap-16 py-20 pt-10 sm:gap-20 md:gap-24 lg:py-32 lg:pt-16"
	>
		<div
			class="relative flex flex-col gap-2 py-4 text-center before:absolute before:top-0 before:left-0 before:h-1.5 before:w-2/3 before:bg-violet-700 after:absolute after:right-0 after:bottom-0 after:h-1.5 after:w-2/3 after:bg-violet-700"
		>
			<h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
			<h3 class="text-3xl font-semibold sm:text-4xl md:text-5xl">
				A bit <span class="poppins text-violet-400">about</span> me.
			</h3>
		</div>
		<p class="poppins mx-auto text-lg font-semibold sm:text-xl md:text-2xl">I am . . .</p>
		<div class="mx-auto flex w-full max-w-[800px] flex-col gap-20">
			{#each benefits as benefit, index}
				<div class="flex gap-6 sm:gap-8">
					<p class="poppins text-4xl font-semibold text-slate-500 sm:text-5xl md:text-6xl">
						0{index + 1}
					</p>
					<div class="flex flex-col gap-6 sm:gap-8">
						<h3 class="text-2xl sm:text-3xl md:text-5xl">
							{benefit.name}
						</h3>
						<p>{benefit.description}</p>
					</div>
				</div>
			{/each}
		</div>
		<h5 class={' poppins text-center text-2xl font-semibold sm:text-3xl '}>
			The <span class="text-violet-400">Complete</span> Package
		</h5>
		<div class="mx-auto flex w-full max-w-[800px] flex-col gap-10 overflow-x-auto">
			<table class="rounded bg-white text-center text-slate-700">
				<thead class={'border-b border-solid border-slate-200  '}>
					<tr class="">
						<th></th>
						<th class="p-2 px-4 whitespace-nowrap">Candidate #1</th>
						<th class="p-2 px-4 whitespace-nowrap">Candidate #2</th>
						<th class="p-2 px-4 whitespace-nowrap">Candidate #3</th>
						<th class="bg-violet-700 p-4 px-8 whitespace-nowrap text-white">Me</th>
					</tr>
				</thead>
				<tbody>
					<tr class="border-b border-solid border-slate-200">
						<td class="border-r border-solid border-white py-4 pr-8 pl-4 text-sm font-semibold">
							Dedication
						</td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-slate-500"></i></td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-green-500"></i></td>
					</tr>
					<tr class="border-b border-solid border-slate-200">
						<td class="border-r border-solid border-white py-4 pr-8 pl-4 text-sm font-semibold">
							Analytical
						</td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-slate-500"></i></td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-green-500"></i></td>
					</tr>
					<tr class="border-b border-solid border-slate-200">
						<td class="border-r border-solid border-white py-4 pr-8 pl-4 text-sm font-semibold">
							Detail-oriented
						</td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-slate-500"></i></td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-green-500"></i></td>
					</tr>
					<tr class="border-b border-solid border-slate-200">
						<td class="border-r border-solid border-white py-4 pr-8 pl-4 text-sm font-semibold">
							Collaborative
						</td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-slate-500"></i></td>
						<td><i class="fa-solid fa-xmark text-slate-500"></i></td>
						<td><i class="fa-solid fa-check text-green-500"></i></td>
					</tr>
				</tbody>
			</table>
		</div>

		<div class="mx-auto -mt-12 italic opacity-50 sm:hidden">
			<p>Scroll to see more &rarr;</p>
		</div>
		<p class="mx-auto">So why not invest?</p>

		<section id="resume" class="mt-20 flex flex-col items-center gap-6">
			<h3 class="text-center text-2xl font-semibold sm:text-3xl md:text-4xl">
				Want the full scoop?
			</h3>
			<p class="text-center text-base sm:text-lg md:text-xl">
				You can download my resume or preview it in your browser.
			</p>

			<div class="flex flex-wrap justify-center gap-4">
				<!-- Preview Button -->
				<button
					on:click={previewResume}
					type="button"
					class="poppins group rounded-full bg-blue-600 px-6 py-3 text-white shadow-md transition hover:bg-blue-700 sm:text-lg md:text-xl"
				>
					<i class="fa-solid fa-eye mr-2"></i>
					Preview Resume
				</button>

				<!-- Download Button -->
				<button
					on:click={downloadResume}
					type="button"
					class="poppins group rounded-full bg-violet-700 px-6 py-3 text-white shadow-md transition hover:bg-violet-800 sm:text-lg md:text-xl"
				>
					<i class="fa-solid fa-download mr-2"></i>
					Download Resume
				</button>
			</div>
		</section>
	</section>
</main>
