<script lang="ts">

  import { drawerStore } from '@skeletonlabs/skeleton';

  function drawerClose(): void {
	drawerStore.close();
  }

</script>

<nav class="text-center p-4 ">
	<ul class="text-right">
		<h2 class="p-4 h4 font-bold text-lg pr-8">Bald Man Brands</h2>
	    <hr/>
		<div class="font-semibold pr-8">
		  <li class="mt-6 text-lg"><a on:click={drawerClose} href="/">Home</a></li>
		  <li class="mt-6 text-lg"><a on:click={drawerClose} href="/about">About</a></li>
		  <li class="mt-6 text-lg"><a on:click={drawerClose} href="/contact">Contact</a></li>
	    </div>
		<hr class="my-4"/>
		<div class="px-8 py-6">
			<div class="-my-2 space-y-4">
				<a class="inline-flex justify-center rounded-lg text-sm font-semibold py-3 px-4 btn variant-filled bg-primary-500 w-full" href="/contact">
					<span>Get Started for Free <span aria-hidden="true">→</span></span></a>
				</div>
			</div>
		<div class="flex items-center justify-center mt-4">
		</div>
	</ul>
</nav>