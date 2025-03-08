<script>
	import Chapitre1 from '$lib/components/istqb_v4.0_fr/Chapitre1.svelte';
	import Chapitre2 from '$lib/components/istqb_v4.0_fr/Chapitre2.svelte';
	import Chapitre3 from '$lib/components/istqb_v4.0_fr/Chapitre3.svelte';
	import Chapitre4 from '$lib/components/istqb_v4.0_fr/Chapitre4.svelte';
	import Chapitre5 from '$lib/components/istqb_v4.0_fr/Chapitre5.svelte';
	import Chapitre6 from '$lib/components/istqb_v4.0_fr/Chapitre6.svelte';
	import Documents from '$lib/components/istqb_v4.0_fr/Documents.svelte';
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
				<label for="my-drawer" class="btn btn-primary drawer-button bg-blue-700 p-6 font-extrabold"
					>Open <i class="fa-solid fa-indent"></i></label
				>
			</div>
			<div class="drawer-side">
				<label for="my-drawer" aria-label="close sidebar" class="drawer-overlay"></label>

				<Sidebar />
			</div>
		</div>
	</div>

	<div class=" mx-auto mt-10 min-h-screen w-full p-4 text-center">
		{#if $x === 1}
			<br />
			<h1 class="text-lg font-bold">Chapitre 1 :</h1>
			<Chapitre1 />
		{:else if $x === 2}
			<br />
			<h1 class="text-lg font-bold">Chapitre 2 :</h1>
			<Chapitre2 />
		{:else if $x === 3}
			<br />
			<h1 class="text-lg font-bold">Chapitre 3 :</h1>
			<Chapitre3 />
		{:else if $x === 4}
			<br />
			<h1 class="text-lg font-bold">Chapitre 4 :</h1>
			<Chapitre4 />
		{:else if $x === 5}
			<br />
			<h1 class="text-lg font-bold">Chapitre 5 :</h1>
			<Chapitre5 />
		{:else if $x === 6}
			<br />
			<h1 class="text-lg font-bold">Chapitre 6 :</h1>
			<Chapitre6 />
		{:else}
			<br />
			<Documents />
		{/if}
	</div>
</div>
