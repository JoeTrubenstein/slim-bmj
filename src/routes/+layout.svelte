<script lang="ts">
	// The ordering of these imports is critical to your app working properly
	import '../theme.postcss';

	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/skeleton.css';

	// Most of your app wide CSS should be put in this file
	import '../app.postcss';

	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	import Navigation from '$lib/Navigation/Navigation.svelte';
	import { Drawer, drawerStore } from '@skeletonlabs/skeleton';
	import { LightSwitch } from '@skeletonlabs/skeleton';

	function drawerOpen(): void {
		drawerStore.open({});
	}
</script>

<!-- Drawer Overlay -->
<Drawer>
	<Navigation />
</Drawer>

<!-- App Shell -->
<AppShell>
	<svelte:fragment slot="header">
		<div class="">
			<!-- App Bar -->
			<AppBar class="lg:px-12 px-4b" background="bg-white border dark:bg-slate-800 dark:border-0">
				<!-- Lead -->
				<svelte:fragment slot="lead">
					<strong class="text-lg">Bald Man Brands</strong>
				</svelte:fragment>

				<!-- Trail -->
				<svelte:fragment slot="trail">
					<div class="hidden md:block">
						<a href="/about" class="btn btn-m variant-ghost-surface">About</a>
						<a href="/contact" class="btn btn-m variant-ghost-surface">Contact</a>
					</div>
					<LightSwitch class="hidden md:block" />
					<div class="flex items-center">
						<button on:click={drawerOpen} class="md:hidden btn btn-sm mr-4">
							<span>
								<svg viewBox="0 0 100 80" class="fill-token w-4 h-4">
									<rect width="100" height="20" />
									<rect y="30" width="100" height="20" />
									<rect y="60" width="100" height="20" />
								</svg>
							</span>
						</button>
					</div>
				</svelte:fragment>
			</AppBar>
		</div>
	</svelte:fragment>
	<!-- Left Sidebar Slot -->
	<div class="container mx-auto">
		<!-- Page Route Content -->
		<slot />
	</div></AppShell>

<style>
	strong {
	    font-family: Raleway;
	}
</style>