<script>
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();

	export let color = 'blue';
	export let text;

	const colors = {
		blue: 'bg-blue-500 hover:bg-blue-700 active:bg-blue-900',
		red: 'bg-red-500 hover:bg-red-700 active:bg-red-900'
	};

	// function dispatch
	function defaultFn() {
		dispatch('toggle', {});
	}
</script>

<button
	on:click={defaultFn}
	class="{colors[color]}
		 rounded-md px-4 py-2 mx-4 text-white transition ease-linear duration-150`}
"
>
	<!-- TODO: use classList and check if the 1st element in the returned array is undefined -->
	<!-- https://developer.mozilla.org/en-US/docs/Web/API/Element/classList -->
	{colors[color] === 'undefined' ? 'use a supported color' : text}
</button>
