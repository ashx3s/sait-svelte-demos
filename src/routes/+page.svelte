<script>
	// render html with @html in the rendered variable { ... }
	const dailyContent = '<span class="text-blue-500">Course Content</span>';
	const description =
		'This is a course about svelte. we learn how to make modern and cool websites with it.';
</script>

<h1 class="text-5xl">SAIT Svelte {@html dailyContent}</h1>
<p>{description}</p>

<div class="bg-blue-100 rounded-sm p-4 max-w-sm">
	<h3 class="text-xl pb-2">The Message</h3>
	<p class="text-gray-500">
		Lorem ipsum dolor sit, amet consectetur adipisicing elit. Consequatur, laborum.
	</p>
</div>

<p>
	Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum neque deserunt aut consequatur
	necessitatibus laboriosam animi dolorem unde minima ut?
</p>
