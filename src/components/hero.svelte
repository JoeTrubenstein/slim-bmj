<script>
  import logo from '$lib/assets/bmbsquare.webp';
  import widelogo from '$lib/assets/bmbwide.webp'
</script>

<section
  class="grid lg:grid-cols-2 place-items-center pb-8 md:pt-12 md:pb-24 lg:px-12 px-4 lg:mt-12 lg:place-items-start">
  
  <div class="py-6 lg:order-1 md:flex hidden w-full items-center justify-center">

    	<!-- Animated Logo -->
		<figure>
			<section class="img-bg" />
            <img
            class="w-72 h-72"
			loading="lazy"
            src={logo}
            alt="Bald Man Brands"
          />
		</figure>
		<!-- / -->

  </div>

  <!--  -->
    <div class="py-6 lg:order-1 md:hidden block">
    		<!-- Animated Logo -->

		<!-- <figure>
			<section class="img-bg" />
            <img
            class="h-48 w-full object-scale-down	"
            src={widelogo}
            alt="Bald Man Brands"
          />
		</figure> -->

		<!-- / -->
  </div>



  <div class="lg:text-left md:text-center text-left">
    <h1
      class="text-4xl lg:text-6xl xl:text-7xl tracking-tighter font-black text-primary-500 dark:text-white">
      Bald Man Brands
    </h1>
	<h2
	class="text-3xl lg:text-5xl xl:text-6xl tracking-tighter font-black text-indigo-600 dark:text-indigo-400">
	really fast websites
  </h2>
    <p class="text-lg mt-4 max-w-xl font-light text-gray-900 md:text-lg dark:text-gray-400">
      Boutique web development and digital marketing from Japan.<wbr> I make hand-coded websites and data-driven ad campaigns that outperform and outshine.
    </p>
    <div class="mt-6 flex flex-col sm:flex-row gap-3 md:justify-center lg:justify-start">
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

	h1, h2 {
		font-family: Montserrat;
	}
</style>