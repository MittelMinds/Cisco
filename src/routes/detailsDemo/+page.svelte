<script>
	import { Card, Button, Toggle, Badge } from 'flowbite-svelte';
	import { ArrowRightOutline, InfoCircleOutline } from 'flowbite-svelte-icons';

	import SelectionCard from '/src/lib/components/selectionCard.svelte';
</script>

<svelte:head>
	<title>Search</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="mt-4">
	<h1 class="mb-2 text-3xl font-semibold">Group Training Session</h1>

	<p class="mb-6">by: Know - Die Fortbildungsagentur.</p>

    <p class="mb-4">This is a shared in-person training session with two other companies of similar size and needs.</p>

    <div class="outline outline-1 p-4 mb-2 pb-4 rounded w-fit">
    <p class="mb-2">Collaboration Partners:</p>
    <p>Familienbäckerei Franz (20 participants)</p>
    <a href="/detailsDemo" class="text-blue-500">view profile</a>
    <p class="mt-2">Kfz-Werkstatt FixNix (22 participants)</p>
    <a href="/detailsDemo" class="text-blue-500">view profile</a>
    </div>
    <p class="mt-4">Total cost: 450,76€</p> 
    <p class="mt-4">Location: Arcisstr. 21, 80333 München</p>
    <p class="mt-4">Date: 27/02/2024, 10:30am</p>
    <Button href="confirmation" class="mt-4 w-1/3" color="green">Register</Button>
		
	<p class="flex text-sm text-gray-600 mt-4"><InfoCircleOutline class="mr-2"/> Collaboration partners and participant counts may change. <a href="/detailsDemo" class="text-blue-500 ml-2">(learn more)</a></p>	

	
</div>
