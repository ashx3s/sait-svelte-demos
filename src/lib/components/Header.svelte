<script>
	const navItems = [
		{ name: 'Home', href: '/' },
		{ name: 'About', href: '/about' },
		{ name: 'Blog', href: '/blog' },
		{ name: 'Products', href: '/products' }
	];
</script>

<header class="bg-black text-white flex justify-between p-4">
	<div>logo</div>
	<nav>
		<ul class="flex justify-around gap-4">
			{#each navItems as { name, href }}
				<li><a {href}>{name}</a></li>
			{/each}
		</ul>
	</nav>
</header>
