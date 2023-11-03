<script>
	import ListItem from '../../lib/components/ListItem.svelte';
	let listItems = ['Dog', 'Cat', 'Crow ', 'Ferret'];
	let secondList = [
		{ name: 'Alfred', species: 'Dog', href: '/' },
		{ name: 'Elvira', species: 'Cat', href: '/' },
		{ name: 'Sally', species: 'Crow', href: '/' },
		{ name: 'Gus', species: 'Ferret', href: '/' }
	];
</script>

<header class="my-4 text-center text-5xl">
	<h1>About Page</h1>
</header>

<section>
	<h2 class="text-3xl">Our Example List</h2>
	<ul class="list-disc ml-8">
		{#each listItems as item}
			<ListItem>{item}</ListItem>
		{/each}
	</ul>
</section>

<section>
	<h2 class="text-3xl">Animals</h2>
	<ul>
		{#each secondList as { href, name, species }}
			<ListItem><a {href}>{name} is a {species}</a></ListItem>
		{/each}
	</ul>
</section>
