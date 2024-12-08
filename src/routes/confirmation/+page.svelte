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
	<h1 class="mb-2 text-3xl font-semibold">Registration Successful</h1>

    <p class="mb-8">You will recieve a confirmation E-Mail with payment instructions shortly.</p>

    <div class="outline outline-1 p-4 mb-2 pb-4 rounded w-fit">
    <p class="mb-4 text-xl text-gray-500">Your Booking</p>
    <p>Cybersecurity Training</p>
    <p class="mt-2">Location: Arcisstr. 21, 80333 München</p>
    <p class="mt-2">Date: 27/02/2024, 10:30am</p>
    <p class="mt-2">Payment Due: 450,76€</p> 
    </div>

	
</div>
