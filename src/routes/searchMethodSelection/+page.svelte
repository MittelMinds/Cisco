<script>
	import { Card, Button, Toggle } from 'flowbite-svelte';
	import { ArrowRightOutline } from 'flowbite-svelte-icons';

	import SelectionCard from "/src/lib/components/selectionCard.svelte"
	
  </script>

<svelte:head>
	<title>Search</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="ml-8 mt-4">
	<h1 class="text-3xl font-semibold mb-2">How would you like to search?</h1>

	<p class="mb-6">
		Please select one of the following methods.
	</p>

	<div class="flex space-x-4">
					
			<SelectionCard imgsrc="/src/lib/images/ai_bot_image.webp" title="Use our AI Assistant" subtitle="Let it interactively guide you towards finding the perfect partner." buttonlabel="Let's go"/>

			<SelectionCard imgsrc="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0b/Search_Icon.svg/1024px-Search_Icon.svg.png" title="Search manually" subtitle="Use keywords and filters to find what you're looking for." buttonlabel="Search"/>
		
	</div>


</div>
