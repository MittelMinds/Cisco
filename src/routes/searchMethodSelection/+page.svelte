<script>
	import { Card, Button, Toggle } from 'flowbite-svelte';
	import { ArrowRightOutline } from 'flowbite-svelte-icons';
	
  </script>

<svelte:head>
	<title>Search</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="bg-amber-400">
	<h1 class="text-3xl font-semibold mb-2">How would you like to search?</h1>

	<p class="mb-4">
		Please select one of the following methods.
	</p>

	<div class="flex space-x-4">
		<div>

			<Card class="">
			<img class="h-28 w-28" src="/src/lib/images/ai_bot_image.webp" alt="bot">
			  <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Use our AI Assistant</h5>
			  <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">Let it interactively guide you towards finding the perfect partner.</p>
			  <Button>
				Let's go <ArrowRightOutline class="w-6 h-6 ms-2 text-white" />
			  </Button>
			</Card>
			
		  </div>

		  <div class="">
			<Card>
			<img class="h-28 w-28" src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0b/Search_Icon.svg/1024px-Search_Icon.svg.png" alt="bot">
			  <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Search manually</h5>
			  <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">Use keywords and filters to find what you're looking for.</p>
			  <Button>
				Start search
			  </Button>
			</Card>
			
		  </div>
	</div>


</div>
