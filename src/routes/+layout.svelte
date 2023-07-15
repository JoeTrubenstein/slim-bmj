<script lang="ts">
	// The ordering of these imports is critical to your app working properly
	import '../theme.postcss';

	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/skeleton.css';

	// Most of your app wide CSS should be put in this file
	import '../app.postcss';

	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	import Navigation from '$lib/Navigation/Navigation.svelte';
	import Footer from '../lib/components/footer.svelte';
	import { Drawer, drawerStore } from '@skeletonlabs/skeleton';
	import { LightSwitch } from '@skeletonlabs/skeleton';
	import hljs from 'highlight.js';
	import 'highlight.js/styles/tokyo-night-dark.css';
	import { storeHighlightJs } from '@skeletonlabs/skeleton';

    storeHighlightJs.set(hljs);

	function drawerOpen(): void {
		drawerStore.open({});
	}

</script>

<!-- Drawer Overlay -->
<Drawer bgDrawer="bg-white dark:bg-slate-800">
	<Navigation />
</Drawer>

<!-- App Shell -->
<AppShell>
	<svelte:fragment slot="header">
		<div>
			<!-- App Bar -->
			<AppBar
				slotDefault="place-self-center"
				class="lg:px-12 px-4b"
				background="bg-white border dark:bg-slate-800 dark:border-0"
			>
				<!-- Lead -->
				<svelte:fragment slot="lead">
					<a href="../"><strong class="text-lg">Bald Man Brands</strong></a>
				</svelte:fragment>
				<div class="hidden md:flex gap-4 -mx-28">
					<a href="../" class="font-bold">Home</a>
					<a href="/about" class="font-bold">About</a>
					<a href="/contact" class="font-bold">Contact</a>
				</div>

				<!-- Trail -->
				<svelte:fragment slot="trail">
					<div class="hidden md:block" />
					<LightSwitch class="block" />
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

	<!-- Page Route Content -->
	<slot />

	<Footer />
</AppShell>