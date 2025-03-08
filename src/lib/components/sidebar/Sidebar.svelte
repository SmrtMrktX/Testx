<script>
	import { x } from './store.js';
	let myCustomBtn = 'p-4 text-left hover:cursor-pointer hover:text-green-600 ';

	// @ts-ignore
	function updateX(value) {
		x.set(value);
	}
</script>

<div
	style="font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif; color: #eaf8e7;"
	class="flex min-h-full w-72 flex-col bg-slate-900 py-8 text-base font-semibold md:w-80 md:text-lg"
>
	<button class={myCustomBtn} on:click={() => updateX(1)}>1. Fondamentaux des tests</button>
	<button class={myCustomBtn} on:click={() => updateX(2)}
		>2. Tester tout au long du cycle de développement logiciel</button
	>
	<button class={myCustomBtn} on:click={() => updateX(3)}>3. Test statique</button>
	<button class={myCustomBtn} on:click={() => updateX(4)}>4. Analyse et conception des tests</button
	>
	<button class={myCustomBtn} on:click={() => updateX(5)}>5. Gestion des activités de test</button>
	<button class={myCustomBtn} on:click={() => updateX(6)}>6. Outils de test</button>
	<button
		style="font-style: italic; margin-top:2rem;"
		class={myCustomBtn}
		on:click={() => updateX(7)}><i class="fa-solid fa-file-pdf"></i> Documents</button
	>

	<div class="badge badge-success mt-20 self-center">ISTQB Foundation Level v4.0</div>
</div>
