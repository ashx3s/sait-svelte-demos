<script>
	import PageHeader from '$lib/components/PageHeader.svelte';
	const pageInfo = {
		title: 'Products',
		description: 'Demonstrating events with a carousel',
		bgColor: 'bg-purple-500'
	};

	// slide array to loop through
	const slideArr = ['dog', 'cat', 'crow', 'ferret', 'iguana'];

	// current index counter
	let currentSlideIndex = 0;

	// current slide content
	let currentSlideContent = slideArr[0];

	// the max length of the array
	const maxLength = slideArr.length - 1;

	// next function
	function nextSlide() {
		if (currentSlideIndex === maxLength) {
			currentSlideIndex = 0;
			currentSlideContent = slideArr[currentSlideIndex];
		} else {
			currentSlideIndex++;
			currentSlideContent = slideArr[currentSlideIndex];
		}
	}

	// previous function
	function prevSlide() {
		if (currentSlideIndex === 0) {
			currentSlideIndex = maxLength;
			currentSlideContent = slideArr[currentSlideIndex];
		} else {
			currentSlideIndex--;
			currentSlideContent = slideArr[currentSlideIndex];
		}
	}
</script>

<PageHeader {...pageInfo} />

<section class="px-4">
	<h2 class="text-2xl font-semibold">{currentSlideIndex}: {currentSlideContent}</h2>
	<div class="mt-2">
		<button on:click={prevSlide} class="rounded-md bg-green-300 px-4 py-2">Previous Slide</button>
		<button on:click={nextSlide} class="rounded-md bg-green-300 px-4 py-2">Next Slide</button>
	</div>
</section>
