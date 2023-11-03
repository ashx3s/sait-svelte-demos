<script>
	// import the MessageBox component
	import MessageBox from '../lib/components/MessageBox.svelte';

	// render html with @html in the rendered variable { ... }
	const dailyContent = '<span class="text-blue-500">Course Content</span>';
	const description =
		'This is a course about svelte. we learn how to make modern and cool websites with it.';

	// pass this into a component:
	const messagesForTheBox = [
		{ title: 'Scooby Doo', description: 'Is a great show' },
		{ title: 'Keyboards are Us', description: 'buy more keyboards' },
		{
			title: 'this is from an object',
			description:
				'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Earum, temporibus. Delectus deserunt soluta, ratione unde dignissimos voluptatem provident pariatur. Eum quod accusantium molestias rerum quidem porro, pariatur fuga id officiis?'
		}
	];
</script>

<h1 class="text-5xl">SAIT Svelte {@html dailyContent}</h1>
<p>{description}</p>

<!-- Render the MessageBox Component -->
{#each messagesForTheBox as box}
	<MessageBox {...box} styles="m-20" />
{/each}

<p>
	Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum neque deserunt aut consequatur
	necessitatibus laboriosam animi dolorem unde minima ut?
</p>
