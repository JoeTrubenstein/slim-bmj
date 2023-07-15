<script>
  import logo from '$lib/assets/bmbsquare.webp';
  import widelogo from '$lib/assets/widebmbmobile.webp'
</script>

<section class="grid lg:grid-cols-2 place-items-center md:pb-24 lg:px-12 px-4 mt-8 lg:mt-12 lg:pt-8 lg:place-items-start">

    <div class="py-6 lg:order-1 sm:flex hidden w-full items-center justify-center">
        <!-- Animated Logo -->
		<figure>
			<section class="img-bg" />
            <img
            class="w-full aspect-square bg-cover bg-center h-72"
            src={logo}
            alt="Bald Man Brands"
          />
		</figure>
		<!-- / -->
    </div>

  <div class="lg:text-left sm:text-center text-left">
	<h1 class="text-slate-900 font-extrabold text-4xl sm:text-5xl lg:text-6xl tracking-tight dark:text-white">Bald Man Brands</h1>
	<h2
	class="text-3xl lg:text-5xl xl:text-6xl tracking-tight lg:tracking-tighter font-extrabold text-indigo-600 dark:text-indigo-400 leading-normal">
	really fast websites
  </h2>
    <p class="text-lg mt-4 max-w-xl leading-relaxed text-gray-900 md:text-lg dark:text-gray-400">
      Boutique web development and digital marketing from Japan.<wbr> Hand-coded websites and data-driven ad campaigns that outperform and outshine.
    </p>

<!-- Mobile Image -->
<div class="py-6 sm:hidden block">
	<img
		class="w-full rounded-lg aspect-video bg-cover bg-center"
		src={widelogo}
		alt="Bald Man Brands"
	/>
  </div>
<!-- / Mobile Image  -->


<div class="sm:mt-6 mt-2 flex flex-col sm:flex-row gap-3 sm:justify-center lg:justify-start">
	<button type="button" class="btn variant-filled bg-primary-500">See how</button>
    <button type="button" class="btn variant-filled bg-primary-500">
	    <span>Get started for free</span>  
    </button>
</div>

  </div>
</section>

<style lang="postcss">
	figure {
		@apply flex relative flex-col;
	}
	/* figure svg, */
	.img-bg {
		@apply w-64 h-64 md:w-80 md:h-80;
	}
	.img-bg {
		@apply absolute z-[-1] rounded-full blur-[50px] transition-all;
		animation: pulse 5s cubic-bezier(0, 0, 0, 0.5) infinite,
			glow 5s linear infinite;
	}
	@keyframes glow {
		0% {
			@apply bg-primary-400/50;
		}
		33% {
			@apply bg-secondary-400/50;
		}
		66% {
			@apply bg-tertiary-400/50;
		}
		100% {
			@apply bg-primary-400/50;
		}
	}
	@keyframes pulse {
		50% {
			transform: scale(1.5);
		}
	}
</style>