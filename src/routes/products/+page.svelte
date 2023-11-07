<script>
	import PageHeader from '$lib/components/PageHeader.svelte';
	import Carousel from '$lib/components/Carousel.svelte';
	const pageInfo = {
		title: 'Products',
		description: 'Demonstrating events with a carousel',
		bgColor: 'bg-purple-500'
	};
</script>

<PageHeader {...pageInfo} />

<Carousel />
