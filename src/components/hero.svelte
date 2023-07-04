<script>
  import logo from '$lib/assets/logo.png';
</script>


<section
  class="grid lg:grid-cols-2 place-items-center pb-8 md:pt-12 md:pb-24 lg:px-12 px-4 mt-12 lg:mt-0 2xl:place-items-start 2xl:justify-center 2xl:items-center">
  <div class="py-6 lg:order-1 md:block hidden 2xl:ml-44">
    		<!-- Animated Logo -->
		<figure>
			<section class="img-bg" />
            <img
            class="lg:w-72 md:w-72"
            src={logo}
            alt="Bald Man Brands"
          />
		</figure>
		<!-- / -->
  </div>
  <div class="lg:text-left md:text-center text-left">
    <h1
      class="text-4xl lg:text-6xl xl:text-7xl lg:tracking-tighter  font-black text-primary-500 dark:text-white">
      Bald Man Brands
    </h1>
	<h1
	class="text-4xl lg:text-6xl xl:text-7xl lg:tracking-tighter font-black text-indigo-600 dark:text-indigo-400">
	really fast websites
  </h1>
    <p class="text-lg mt-4 max-w-xl text-primary-500 dark:text-gray-200">
      Web development and digital marketing by a bald man in Japan.<wbr> I make hand-coded websites that outperform and outshine.
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
</style>