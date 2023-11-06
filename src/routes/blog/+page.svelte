<script>
	import PageHeader from '../../lib/components/PageHeader.svelte';

	const headerInfo = {
		title: 'Blog',
		description: 'This is a blog about tech and mystery machines.',
		bgColor: 'bg-blue-500'
	};
</script>

<PageHeader {...headerInfo} />
