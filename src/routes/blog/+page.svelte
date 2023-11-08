<script>
	import PageHeader from '../../lib/components/PageHeader.svelte';

	const headerInfo = {
		title: 'Blog',
		description: 'This is a blog about tech and mystery machines.',
		bgColor: 'bg-blue-500'
	};
	// TODO: address capitalization on input (strings should be able to be lowercase but always return proper capitalized)
	const user = {
		name: 'Ash',
		login: true
	};

	// Simple Alert Toggle
	const userLoginToggle = () => {
		user.login = !user.login;
	};

	function greet() {
		if (user.login) {
			alert('Hello World');
		}
	}
</script>

<PageHeader {...headerInfo} flexContent>This is for the flex content box</PageHeader>

{#if user.name === 'Godfrey'}
	<p>Stop trying to hack my system Godfrey</p>
{:else if user.name === 'Ash'}
	<p>Good morning {user.name}, even in the afternoon</p>
{:else}
	<p>Hello {user.name}</p>
{/if}

<section class="my-4">
	<h2 class="my-2 text-2xl font-semibold ml-4">Toggles</h2>
	<button
		on:click={greet}
		class="rounded-md bg-red-500 px-4 py-2 mx-4 text-white transition ease-linear duration-150 hover:bg-red-700 active:bg-red-900"
		>Send Alert</button
	>
	<button
		on:click={userLoginToggle}
		class="rounded-md bg-blue-500 px-4 py-2 mx-4 text-white transition ease-linear duration-150 hover:bg-blue-700 active:bg-blue-900"
		>Toggle User Login</button
	>
</section>

{#if user.login === true}
	<p>{user.name}, Welcome to the site</p>
{:else}
	<section class="my-12">
		<!-- buttons for alert toggle -->
		<p class="text-5xl ml-4">{user.login}</p>
	</section>
{/if}
