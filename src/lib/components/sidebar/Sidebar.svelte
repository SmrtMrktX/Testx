<script>
	import { x } from './store.js';
	let myCustomBtn = 'p-4 text-left hover:cursor-pointer hover:bg-slate-900 ';

	// @ts-ignore
	function updateX(value) {
		x.set(value);
	}
</script>

<div
	style="font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;"
	class="flex min-h-full w-72 flex-col bg-slate-950 py-8 text-lg font-semibold text-yellow-400 md:w-80 md:text-xl xl:w-96"
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
	<button class={myCustomBtn} on:click={() => updateX(7)}>The End</button>
</div>
