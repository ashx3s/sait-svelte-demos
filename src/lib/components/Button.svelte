<script>
	export let colors = {
		main: 'bg-blue-500',
		hover: 'bg-blue-700',
		active: 'bg-blue-900'
	};
	export let text;
	// function
</script>

<button
	class="{colors.main} hover:{colors.hover} active:{colors.active} rounded-md px-4 py-2 mx-4 text-white transition ease-linear duration-150"
>
	{text}
</button>
