<script>
	import { Card, Button, Toggle, Badge } from 'flowbite-svelte';
	import { ArrowRightOutline } from 'flowbite-svelte-icons';

	import SelectionCard from '/src/lib/components/selectionCard.svelte';
</script>

<svelte:head>
	<title>Search</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="mt-4">
	<h1 class="mb-2 text-3xl font-semibold">Offers for you</h1>

	<p class="mb-6">Here are some great collab opportunities!</p>

	<div class="flex space-x-4">
		
		<Card class="h-fit">
			<Badge border color="green" class="w-fit mb-4">Recommended</Badge>
			<h5 class="mb-2 text-2xl font-semibold tracking-tight text-gray-900 dark:text-white">Group Training Session</h5>
			<p class="mb-3 font-normal leading-tight text-gray-700 dark:text-gray-400">Share a training session with two other companies of a similar size and save on the rate.</p>
			<p class="mb-3 font-normal leading-tight text-gray-700 dark:text-gray-400">Provider: Know - Die Fortbildungsagentur.</p>
			<p class="mb-3 font-normal leading-tight text-gray-700 dark:text-gray-400">Type: in-person</p>
			<p class="mb-3 font-normal leading-tight text-gray-700 dark:text-gray-400">Distance: less than 10km</p>
			<p class="mb-3 font-normal leading-tight text-gray-700 dark:text-gray-400">Date: 27/02/2024, 10:30am</p>
			<div class="outline outline-1 pt-2 pl-2 mb-2 rounded">
			<p class="mb-3 font-normal leading-tight text-gray-700 dark:text-gray-400">Total cost: 450,76€</p>
			</div>
			<Button href="detailsDemo" color="dark" class="mt-2">
				Learn more <ArrowRightOutline class="ml-2"/>
			</Button>
		</Card>

		<Card class="h-fit">
			<Badge border color="red" class="w-fit mb-4">% Budget Pick</Badge>
			<h5 class="mb-2 text-2xl font-semibold tracking-tight text-gray-900 dark:text-white">Zoom Training Session</h5>
			<p class="mb-3 font-normal leading-tight text-gray-700 dark:text-gray-400">Take part in a zoom meeting training session held to approx. 300 people.</p>
			<p class="mb-3 font-normal leading-tight text-gray-700 dark:text-gray-400">Provider: EduTech Germany</p>
			<p class="mb-3 font-normal leading-tight text-gray-700 dark:text-gray-400">Type: online</p>
			<p class="mb-3 font-normal leading-tight text-gray-700 dark:text-gray-400">Date: 23/02/2024, 9:00am</p>
			<div class="outline outline-1 pt-2 pl-2 mb-2 rounded">
			<p class="mb-3 font-normal leading-tight text-gray-700 dark:text-gray-400">Total cost: 100,48€</p>
			</div>
			<Button color="dark" class="mt-2">
				Learn more <ArrowRightOutline class="ml-2"/>
			</Button>
		</Card>

		<Card class="h-fit">
			<Badge border color="yellow" class="w-fit mb-4">High-Quality</Badge>
			<h5 class="mb-2 text-2xl font-semibold tracking-tight text-gray-900 dark:text-white">Private Consultancy Service</h5>
			<p class="mb-3 font-normal leading-tight text-gray-700 dark:text-gray-400">Book a private training session for your team.</p>
			<p class="mb-3 font-normal leading-tight text-gray-700 dark:text-gray-400">Provider: Ludwigsberger IT Consulting München</p>
			<p class="mb-3 font-normal leading-tight text-gray-700 dark:text-gray-400">Type: in-person</p>
			<p class="mb-3 font-normal leading-tight text-gray-700 dark:text-gray-400">Distance: less than 3km</p>
			<p class="mb-3 font-normal leading-tight text-gray-700 dark:text-gray-400">Date: 21/02/2024, 11:30am</p>
			<div class="outline outline-1 pt-2 pl-2 mb-2 rounded">
				<p class="mb-3 font-normal leading-tight text-gray-700 dark:text-gray-400">Total cost: 2580,79€</p>
			</div>
			
			<Button color="dark" class="mt-2">
				Learn more <ArrowRightOutline class="ml-2"/>
			</Button>
		</Card>

	
	</div>
</div>
