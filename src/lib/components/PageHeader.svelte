<script>
	export let title = 'Placeholder Title';
	export let description = 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum, dolore.';
	export let bgColor = 'bg-gray-200';
</script>

<!-- Header -->
<header class="{bgColor} mb-4 lg:mb-8 text-white py-12 flex flex-col items-center">
	<!-- Title -->
	<h1 class="text-3xl lg:text-5xl font-semibold">{title}</h1>
	<!-- Description -->
	<p class="text-lg lg:text-xl text-center max-w-sm mt-2">{description}</p>
	<!-- Slot for flex content
	<div class="bg-white text-blue-600 rounded-lg p-4">
		<slot />
	</div>
  -->
</header>
