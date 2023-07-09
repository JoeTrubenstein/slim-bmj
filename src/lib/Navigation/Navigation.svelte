<script lang="ts">

  import { drawerStore, LightSwitch } from '@skeletonlabs/skeleton';

  function drawerClose(): void {
	drawerStore.close();
  }

</script>

<nav class="text-center p-4 ">
	<ul class="text-center">
		<h2 class="p-4 h4 font-bold">Bald Man Brands</h2>
	    <hr/>
		<div class="font-bold">
		  <li class="mt-4"><a on:click={drawerClose} href="/">Home</a></li>
		  <li class="mt-4"><a on:click={drawerClose} href="/about">About</a></li>
		  <li class="mt-4"><a on:click={drawerClose} href="/contact">Contact</a></li>
	    </div>
		<div class="flex items-center justify-center mt-4">
         <LightSwitch />
		</div>
	</ul>
</nav>