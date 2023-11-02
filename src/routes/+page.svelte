<script>
	// import the MessageBox component
	import MessageBox from '../lib/components/MessageBox.svelte';

	// render html with @html in the rendered variable { ... }
	const dailyContent = '<span class="text-blue-500">Course Content</span>';
	const description =
		'This is a course about svelte. we learn how to make modern and cool websites with it.';
</script>

<h1 class="text-5xl">SAIT Svelte {@html dailyContent}</h1>
<p>{description}</p>

<!-- Render the MessageBox Component -->
<MessageBox title="Whatever" description="a bunch of text" />
<MessageBox />
<MessageBox />
<p>
	Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum neque deserunt aut consequatur
	necessitatibus laboriosam animi dolorem unde minima ut?
</p>
