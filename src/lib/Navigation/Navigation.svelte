<script lang="ts">

  import { drawerStore } from '@skeletonlabs/skeleton';

  function drawerClose(): void {
	drawerStore.close();
  }

</script>

<nav class="text-center p-4 ">
	<ul class="text-center">
		<h2 class="p-4 h4 font-bold text-2xl">Bald Man Brands</h2>
	    <hr/>
		<div class="font-bold">
		  <li class="mt-4 text-xl"><a on:click={drawerClose} href="/">Home</a></li>
		  <li class="mt-4 text-xl"><a on:click={drawerClose} href="/about">About</a></li>
		  <li class="mt-4 text-xl"><a on:click={drawerClose} href="/contact">Contact</a></li>
	    </div>
		<hr class="my-4"/>
		<div class="flex items-center justify-center mt-4">
		</div>
	</ul>
</nav>

<style>
	ul {
		font-family: Inter;
	}
</style>