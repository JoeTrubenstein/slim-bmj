<script lang="ts">
	import { getImageLink } from '$lib/images';
	import { TabGroup, Tab, ProgressBar } from '@skeletonlabs/skeleton';
    import testlogo from '$lib/assets/bmbsquare.webp'

	// Local
	let theme = 'simple';
	const themeStyles: any = {
		simple: {
			base: 'bg-indigo-200 font-sans rounded-container-token',
			header: 'bg-indigo-600  p-4 grid grid-cols-3 gap-8 items-center rounded-tl-container-token rounded-tr-container-token',
			src: "https://source.unsplash.com/random",
			img: 'bg-black w-full aspect-square rounded-full object-cover',
			text1: 'text-on-primary-token text-lg opacity-75 ',
			text2: 'text-on-primary-token font-bold text-xl sm:text-3xl',
			text3: 'text-on-primary-token text-lg sm:text-2xl ',
			progressTrack: 'bg-primary-400',
			progressMeter: 'bg-white',
			footer: 'p-10 grid grid-cols-5 gap-10 place-items-center rounded-tl-3xl rounded-tr-3xl',
			button: 'btn-icon text-black',
            track: "M+M's",
            artist: "Blink-182",
            link: "https://youtu.be/kZs88WWGDoo"
		},
		elegant: {
			base: 'bg-white text-black font-serif shadow',
			header: 'bg-neutral-100 p-4 grid grid-cols-3 gap-8 items-center',
			src: "https://source.unsplash.com/random",
			img: 'bg-black bg-black/50 w-full aspect-square scale-110 transition-transform',
			text1: 'text-lg opacity-50',
			text2: 'text-xl sm:text-3xl',
			text3: 'text-lg sm:text-2xl',
			progressTrack: 'bg-black/5',
			progressMeter: 'bg-black',
			footer: 'p-10 grid grid-cols-5 gap-10 place-items-center',
			button: 'btn-icon rounded-none text-black ring-[1px] ring-black/5',
            track: "Humoresque No.7 in G flat, Op.101 No. 7",
            artist: "Josef Hassid",
            link: "https://youtu.be/iY1ZNKFX5og"
		},
		playful: {
			base: 'bg-blue-700 text-white font-sans rounded-3xl shadow-xl',
			header: 'bg-blue-800 p-4 grid grid-cols-3 gap-8 items-center rounded-tl-3xl rounded-tr-3xl',
			src: "https://source.unsplash.com/random",
			img: 'bg-black w-full aspect-square rounded-3xl scale-110 -translate-x-4 -translate-y-4 transition-transform',
			text1: 'text-lg text-amber-300',
			text2: 'font-bold text-xl sm:text-3xl',
			text3: 'text-lg sm:text-2xl',
			progressTrack: 'bg-black/5',
			progressMeter: 'bg-white',
			footer: 'p-10 grid grid-cols-5 gap-10 place-items-center rounded-tl-3xl rounded-tr-3xl',
			button: 'btn-icon bg-amber-300 text-blue-900',
            track: "Party Hard",
            artist: "Andrew W.K.",
            link: "https://youtu.be/WccfbPQNMbg"
		},
		brutalist: {
			base: 'bg-black text-white font-mono overflow-hidden',
			header: 'bg-white text-black p-4 grid grid-cols-3 gap-8 items-center',
			src: "https://source.unsplash.com/random",
			img: 'bg-black w-full aspect-square transition-transform border-r-4 border-b-4 border-teal-300',
			text1: 'text-lg text-teal-300',
			text2: 'font-bold text-xl sm:text-3xl',
			text3: 'italic text-lg sm:text-2xl',
			progressTrack: 'bg-teal-300/75',
			progressMeter: 'bg-teal-300',
			footer: 'p-10 grid grid-cols-5 gap-10 place-items-center',
			button: 'btn-icon rounded-none bg-teal-300 text-black ring ring-white',
            track: "Goliath",
            artist: "The Mars Volta",
            link: "https://youtu.be/lrwMMF2QS14"
		}
	};
</script>

<section class="md:pt-6 md:pb-12 lg:px-12 px-4 pt-2 mt-12">
<div class="grid grid-cols-1 lg:grid-cols-2 gap-4 md:gap-10 items-center">
	<!-- Info -->
	<div class="space-y-4 md:space-y-10">
		<div class="max-w-[640px] mx-auto space-y-4 mb-12 sm:mb-0">
			<h2 class="text-3xl lg:text-5xl tracking-tighter font-black text-primary-500 dark:text-white">Express your aesthetic</h2>
			<!-- prettier-ignore -->
			<p class="leading-relaxed text-gray-900 md:text-lg dark:text-gray-400 ">
				Create fully customized thems that <strong class="font-black text-indigo-600 dark:text-indigo-400">look and feel</strong> like your brand.<wbr> Use your existing assets for inspiration or start entirely from scratch. 
			</p>
		</div>
		<!-- Tabs -->
		<TabGroup
			active="variant-filled"
			hover="hover:variant-soft"
			flex="flex-1 lg:flex-none"
			rounded="rounded-container-token"
			border=""
			regionList="space-x-1"
			padding="p-2 sm:p-4"
			class="max-w-[640px] mx-auto text-center"
		>
			<Tab bind:group={theme} name="theme" value="simple" class="space-y-4 w-24">
				<svelte:fragment slot="lead">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6">
                        <path fill-rule="evenodd" d="M3 6a3 3 0 013-3h2.25a3 3 0 013 3v2.25a3 3 0 01-3 3H6a3 3 0 01-3-3V6zm9.75 0a3 3 0 013-3H18a3 3 0 013 3v2.25a3 3 0 01-3 3h-2.25a3 3 0 01-3-3V6zM3 15.75a3 3 0 013-3h2.25a3 3 0 013 3V18a3 3 0 01-3 3H6a3 3 0 01-3-3v-2.25zm9.75 0a3 3 0 013-3H18a3 3 0 013 3V18a3 3 0 01-3 3h-2.25a3 3 0 01-3-3v-2.25z" clip-rule="evenodd" />
                      </svg>                      
                </svelte:fragment>
			    Minimal
			</Tab>
			<Tab bind:group={theme} name="theme" value="elegant" class="space-y-4 w-24">
				<svelte:fragment slot="lead">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6">
                        <path fill-rule="evenodd" d="M7.5 5.25a3 3 0 013-3h3a3 3 0 013 3v.205c.933.085 1.857.197 2.774.334 1.454.218 2.476 1.483 2.476 2.917v3.033c0 1.211-.734 2.352-1.936 2.752A24.726 24.726 0 0112 15.75c-2.73 0-5.357-.442-7.814-1.259-1.202-.4-1.936-1.541-1.936-2.752V8.706c0-1.434 1.022-2.7 2.476-2.917A48.814 48.814 0 017.5 5.455V5.25zm7.5 0v.09a49.488 49.488 0 00-6 0v-.09a1.5 1.5 0 011.5-1.5h3a1.5 1.5 0 011.5 1.5zm-3 8.25a.75.75 0 100-1.5.75.75 0 000 1.5z" clip-rule="evenodd" />
                        <path d="M3 18.4v-2.796a4.3 4.3 0 00.713.31A26.226 26.226 0 0012 17.25c2.892 0 5.68-.468 8.287-1.335.252-.084.49-.189.713-.311V18.4c0 1.452-1.047 2.728-2.523 2.923-2.12.282-4.282.427-6.477.427a49.19 49.19 0 01-6.477-.427C4.047 21.128 3 19.852 3 18.4z" />
                      </svg>
                      
                </svelte:fragment>
				Elegant
			</Tab>
			<Tab bind:group={theme} name="theme" value="playful" class="space-y-4 w-24">
				<svelte:fragment slot="lead">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6">
                        <path fill-rule="evenodd" d="M20.599 1.5c-.376 0-.743.111-1.055.32l-5.08 3.385a18.747 18.747 0 00-3.471 2.987 10.04 10.04 0 014.815 4.815 18.748 18.748 0 002.987-3.472l3.386-5.079A1.902 1.902 0 0020.599 1.5zm-8.3 14.025a18.76 18.76 0 001.896-1.207 8.026 8.026 0 00-4.513-4.513A18.75 18.75 0 008.475 11.7l-.278.5a5.26 5.26 0 013.601 3.602l.502-.278zM6.75 13.5A3.75 3.75 0 003 17.25a1.5 1.5 0 01-1.601 1.497.75.75 0 00-.7 1.123 5.25 5.25 0 009.8-2.62 3.75 3.75 0 00-3.75-3.75z" clip-rule="evenodd" />
                      </svg>                      
                </svelte:fragment>
				Playful
			</Tab>
			<Tab bind:group={theme} name="theme" value="brutalist" class="space-y-4 w-24">
				<svelte:fragment slot="lead">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6">
                        <path fill-rule="evenodd" d="M12 6.75a5.25 5.25 0 016.775-5.025.75.75 0 01.313 1.248l-3.32 3.319c.063.475.276.934.641 1.299.365.365.824.578 1.3.64l3.318-3.319a.75.75 0 011.248.313 5.25 5.25 0 01-5.472 6.756c-1.018-.086-1.87.1-2.309.634L7.344 21.3A3.298 3.298 0 112.7 16.657l8.684-7.151c.533-.44.72-1.291.634-2.309A5.342 5.342 0 0112 6.75zM4.117 19.125a.75.75 0 01.75-.75h.008a.75.75 0 01.75.75v.008a.75.75 0 01-.75.75h-.008a.75.75 0 01-.75-.75v-.008z" clip-rule="evenodd" />
                        <path d="M10.076 8.64l-2.201-2.2V4.874a.75.75 0 00-.364-.643l-3.75-2.25a.75.75 0 00-.916.113l-.75.75a.75.75 0 00-.113.916l2.25 3.75a.75.75 0 00.643.364h1.564l2.062 2.062 1.575-1.297z" />
                        <path fill-rule="evenodd" d="M12.556 17.329l4.183 4.182a3.375 3.375 0 004.773-4.773l-3.306-3.305a6.803 6.803 0 01-1.53.043c-.394-.034-.682-.006-.867.042a.589.589 0 00-.167.063l-3.086 3.748zm3.414-1.36a.75.75 0 011.06 0l1.875 1.876a.75.75 0 11-1.06 1.06L15.97 17.03a.75.75 0 010-1.06z" clip-rule="evenodd" />
                      </svg>                      
                </svelte:fragment>
				Brutalist
			</Tab>
		</TabGroup>
	</div>
	<!-- Card -->
	<div>
		<div class="max-w-[640px] mx-auto transition ease-in-out duration-200 {themeStyles[theme].base}">
			<header class={themeStyles[theme].header}>
				<img src={themeStyles[theme].src} class={themeStyles[theme].img} alt="Cover" />
				<div class="col-span-2 space-y-2">
					<div class={themeStyles[theme].text1}>Bald Man Radio</div>
					<div class={themeStyles[theme].text2}>{themeStyles[theme].track}</div>
					<div class={themeStyles[theme].text3}>{themeStyles[theme].artist}</div>
				</div>
			</header>
			<ProgressBar
				value={75}
				max={100}
				track={themeStyles[theme].progressTrack}
				meter={themeStyles[theme].progressMeter}
				rounded="rounded-none"
			/>
			<footer class={themeStyles[theme].footer}>
				<button class={themeStyles[theme].button}>
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6">
                    <path fill-rule="evenodd" d="M15.75 4.5a3 3 0 11.825 2.066l-8.421 4.679a3.002 3.002 0 010 1.51l8.421 4.679a3 3 0 11-.729 1.31l-8.421-4.678a3 3 0 110-4.132l8.421-4.679a3 3 0 01-.096-.755z" clip-rule="evenodd" />
                  </svg>
                  </button>
				<button class={themeStyles[theme].button}>
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6">
                    <path d="M9.195 18.44c1.25.713 2.805-.19 2.805-1.629v-2.34l6.945 3.968c1.25.714 2.805-.188 2.805-1.628V8.688c0-1.44-1.555-2.342-2.805-1.628L12 11.03v-2.34c0-1.44-1.555-2.343-2.805-1.629l-7.108 4.062c-1.26.72-1.26 2.536 0 3.256l7.108 4.061z" />
                  </svg>
                  </button>
				<a class={themeStyles[theme].button} href={themeStyles[theme].link} target="_blank">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6">
                    <path d="M15 6.75a.75.75 0 00-.75.75V18a.75.75 0 00.75.75h.75a.75.75 0 00.75-.75V7.5a.75.75 0 00-.75-.75H15zM20.25 6.75a.75.75 0 00-.75.75V18c0 .414.336.75.75.75H21a.75.75 0 00.75-.75V7.5a.75.75 0 00-.75-.75h-.75zM5.055 7.06C3.805 6.347 2.25 7.25 2.25 8.69v8.122c0 1.44 1.555 2.343 2.805 1.628l7.108-4.061c1.26-.72 1.26-2.536 0-3.256L5.055 7.061z" />
                  </svg>
                </a>
				<button class={themeStyles[theme].button}>
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6">
                    <path d="M5.055 7.06c-1.25-.714-2.805.189-2.805 1.628v8.123c0 1.44 1.555 2.342 2.805 1.628L12 14.471v2.34c0 1.44 1.555 2.342 2.805 1.628l7.108-4.061c1.26-.72 1.26-2.536 0-3.256L14.805 7.06C13.555 6.346 12 7.25 12 8.688v2.34L5.055 7.06z" />
                  </svg>
                  </button>
				<button class={themeStyles[theme].button}>
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-6 h-6">
                    <path d="M11.645 20.91l-.007-.003-.022-.012a15.247 15.247 0 01-.383-.218 25.18 25.18 0 01-4.244-3.17C4.688 15.36 2.25 12.174 2.25 8.25 2.25 5.322 4.714 3 7.688 3A5.5 5.5 0 0112 5.052 5.5 5.5 0 0116.313 3c2.973 0 5.437 2.322 5.437 5.25 0 3.925-2.438 7.111-4.739 9.256a25.175 25.175 0 01-4.244 3.17 15.247 15.247 0 01-.383.219l-.022.012-.007.004-.003.001a.752.752 0 01-.704 0l-.003-.001z" />
                  </svg>
                  </button>
			</footer>
		</div>
	</div>
</div>

<style>
    h2 {
        font-family: Montserrat;
    }
    .tab-lead {
        display: flex;
        justify-content: center;
        align-items: center;
    }
</style>
</section>