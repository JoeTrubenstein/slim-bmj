<script>

	let features = [
		{
			title: 'Design',
			description: 'Polish an existing project or create something completely new. Explore different theories of web design and find something that gets you excited.',
			icon: 'M21.731 2.269a2.625 2.625 0 00-3.712 0l-1.157 1.157 3.712 3.712 1.157-1.157a2.625 2.625 0 000-3.712zM19.513 8.199l-3.712-3.712-12.15 12.15a5.25 5.25 0 00-1.32 2.214l-.8 2.685a.75.75 0 00.933.933l2.685-.8a5.25 5.25 0 002.214-1.32L19.513 8.2z'
		},
		{
			title: 'Develop',
			description:
				"Hand-coding means having control over every aspect. I use the highest-rated web frameworks available to achieve what page builders can't.",
			icon: 'M14.447 3.027a.75.75 0 01.527.92l-4.5 16.5a.75.75 0 01-1.448-.394l4.5-16.5a.75.75 0 01.921-.526zM16.72 6.22a.75.75 0 011.06 0l5.25 5.25a.75.75 0 010 1.06l-5.25 5.25a.75.75 0 11-1.06-1.06L21.44 12l-4.72-4.72a.75.75 0 010-1.06zm-9.44 0a.75.75 0 010 1.06L2.56 12l4.72 4.72a.75.75 0 11-1.06 1.06L.97 12.53a.75.75 0 010-1.06l5.25-5.25a.75.75 0 011.06 0z'
		},
		{
			title: 'Deploy',
			description:
				'Send your idea out in the world with managed and reliable hosting. Utilize advanced SEO and analytic tools to grow your online endeavor.',
			icon: 'M10.5 3.75a6 6 0 00-5.98 6.496A5.25 5.25 0 006.75 20.25H18a4.5 4.5 0 002.206-8.423 3.75 3.75 0 00-4.133-4.303A6.001 6.001 0 0010.5 3.75zm2.03 5.47a.75.75 0 00-1.06 0l-3 3a.75.75 0 101.06 1.06l1.72-1.72v4.94a.75.75 0 001.5 0v-4.94l1.72 1.72a.75.75 0 101.06-1.06l-3-3z'
		}
	];
</script>

<section class="md:pt-6 pb-12 lg:pb-6 lg:px-12 px-4 pt-2">
	<div class="mt-16 md:mt-0">
		<h2 class="text-slate-900 font-extrabold text-3xl sm:text-4xl lg:text-5xl tracking-tight dark:text-white">
			Everything you need to build an online presence
		</h2>
		<p class="text-lg mt-4 leading-relaxed text-gray-900 md:text-lg dark:text-gray-400">
			A minimalist approach that favors speed, security, and simplicity. No plugins or page
			builders.
		</p>
	</div>

	<div class="grid sm:grid-cols-2 md:grid-cols-3 mt-16 gap-16">
		{#each features as item}
			<div class="flex gap-4 items-start">
				<div
					class="mt-1 bg-primary-500 dark:bg-white rounded-full p-2 w-9 h-9 shrink-0 flex items-center justify-center"
				>
					<svg
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 24 24"
						fill="currentColor"
						class="w-7 h-7 variant-filled"
					>
						<path fill-rule="evenodd" d={item.icon} clip-rule="evenodd" />
					</svg>
				</div>
				<div>
					<h3 class="font-semibold text-lg text-indigo-600 dark:text-indigo-400">{item.title}</h3>
					{' '}
					<p class="mt-2 leading-relaxed text-gray-900 md:text-lg dark:text-gray-400">
						{item.description}
					</p>
				</div>
			</div>
		{/each}
	</div>
</section>
