<script>
	import Chapitre1 from '$lib/components/istqb_v4.0_fr/Chapitre1.svelte';
	import Chapitre2 from '$lib/components/istqb_v4.0_fr/Chapitre2.svelte';
	import Chapitre3 from '$lib/components/istqb_v4.0_fr/Chapitre3.svelte';
	import Chapitre4 from '$lib/components/istqb_v4.0_fr/Chapitre4.svelte';
	import Chapitre5 from '$lib/components/istqb_v4.0_fr/Chapitre5.svelte';
	import Chapitre6 from '$lib/components/istqb_v4.0_fr/Chapitre6.svelte';
	import Sidebar from '$lib/components/sidebar/Sidebar.svelte';
	import { x } from '$lib/components/sidebar/store.js';
</script>

<div class="flex">
	<!-- Sidebar (Visible on medium+ screens) -->
	<div class="hidden min-h-screen justify-start md:flex">
		<Sidebar />
	</div>

	<!-- Page Content -->
	<div class="flex-1 p-4 md:hidden">
		<!-- Open Drawer Button (Only on Mobile) -->
		<div class="drawer">
			<input id="my-drawer" type="checkbox" class="drawer-toggle" />
			<div class="drawer-content">
				<!-- Page content here -->
				<label for="my-drawer" class="btn btn-primary drawer-button p-6 font-semibold"
					>Open drawer</label
				>
			</div>
			<div class="drawer-side">
				<label for="my-drawer" aria-label="close sidebar" class="drawer-overlay"></label>

				<Sidebar />
			</div>
		</div>
	</div>
	<div class=" mx-auto mt-10 w-full p-4 text-center">
		{#if $x === 1}
			<h1 class="text-2xl font-semibold">Chapitre 1 :</h1>
			<Chapitre1 />
		{:else if $x === 2}
			<h1 class="text-2xl font-semibold">Chapitre 2 :</h1>
			<Chapitre2 />
		{:else if $x === 3}
			<h1 class="text-2xl font-semibold">Chapitre 3 :</h1>
			<Chapitre3 />
		{:else if $x === 4}
			<h1 class="text-2xl font-semibold">Chapitre 4 :</h1>
			<Chapitre4 />
		{:else if $x === 5}
			<h1 class="text-2xl font-semibold">Chapitre 5 :</h1>
			<Chapitre5 />
		{:else if $x === 6}
			<h1 class="text-2xl font-semibold">Chapitre 6 :</h1>
			<Chapitre6 />
		{:else}
			<h1 class="text-3xl font-semibold">The End</h1>
		{/if}
	</div>
</div>
