<script>
	import PageHeader from '../../lib/components/PageHeader.svelte';

	const headerInfo = {
		title: 'Blog',
		description: 'This is a blog about tech and mystery machines.',
		bgColor: 'bg-blue-500'
	};
	// TODO: address capitalization on input (strings should be able to be lowercase but always return proper capitalized)
	const name = 'ash';
</script>

<PageHeader {...headerInfo} />

{#if name === 'Godfrey'}
	<p>Stop trying to hack my system Godfrey</p>
{:else if name === 'Ash'}
	<p>Good morning {name}, even in the afternoon</p>
{:else}
	<p>Hello {name}</p>
{/if}

<!-- 
if (input === "Ash") {
    console.log("hello")
    return "hello";
  } else if (input === "Godfrey") {
    console.log("Stop trying to log into my syste Godfrey");
    return "stop hacking Godfrey";
  } else {
    console.log("signed out");
    return "signed out";
  }
 -->
