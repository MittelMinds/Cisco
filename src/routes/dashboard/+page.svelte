<script>
	import Dashboard from '/src/lib/components/Dashboard.svelte';

	import { page } from '$app/stores';
	import { Button, Sidebar, SidebarGroup, SidebarItem, SidebarWrapper } from 'flowbite-svelte';
	import {
		ChartPieSolid,
		GridSolid,
		MailBoxSolid,
		UserSolid,
		ArrowRightToBracketOutline,
		EditOutline,
		ArrowRightOutline
	} from 'flowbite-svelte-icons';
	$: activeUrl = $page.url.pathname;
</script>

<svelte:head>
	<title>Home home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<div class="flex flex-row space-x-4">
		<div class="h-full w-fit">
			<Dashboard />
		</div>

		<div class="ml-4 w-2/3 rounded p-6 text-xl outline outline-1 outline-gray-300 shadow-md">
			<p class="font-xl ml-2 mb-4">My Queries</p>
			<div class="flex flex-row space-x-6">
				<div class="bg-gray-200 outline outline-1 outline-gray-400 p-4 rounded h-fit w-fit">
					<p class="text-md mb-2">Cybersecurity Training</p>
					<p class="text-sm">Scheduled for: 28/02/2024, 10:00am</p>
					<p class="text-sm mb-4">Provided by: Know - Die Fortbilder.</p>
					<Button color="light">manage</Button>
				</div>
				<div class="bg-gray-200 outline outline-1 outline-gray-400 p-4 rounded h-fit w-fit">
					<p class="text-md mb-2 flex flex-row">Epoxy Resin <ArrowRightOutline class="mt-1 mx-2"/> Adhesive Formulation</p>
					<p class="text-sm">Recommendation: Quality Control Innovation</p>
					<p class="text-sm mb-4">Potential partners: 8</p>
					<div class="flex flex-row">
						<Button color="light">manage</Button>
						<div class="grow"></div>
						<img class="ml-2 mt-4 h-6 w-auto" src="/src/lib/images/process-icon.png" alt="icon">
					</div>
					
				</div>
			</div>

			<p class="font-xl ml-2 mt-8 mb-4">My Provided Services</p>
			<div class="flex flex-row space-x-6">
				<div class="bg-gray-200 outline outline-1 outline-gray-400 p-4 rounded h-fit w-fit">
					<p class="text-md mb-2">Machining Service</p>
					<p class="text-sm">Upcoming Appointments: 7</p>
					<p class="text-sm">Total Revenue: 35.4k€</p>
					<p class="text-sm mb-4">Rating: 4/5 (58 reviews)</p>
					<Button color="light">manage</Button>
				</div>
				<div class="bg-gray-200 outline outline-1 outline-gray-400 p-4 rounded h-fit w-fit">
					<p class="text-md mb-2">Tool Sharpening Service</p>
					<p class="text-sm">Upcoming Appointments: 2</p>
					<p class="text-sm">Total Revenue: 2.4k€</p>
					<p class="text-sm mb-4">Rating: 5/5 (45 reviews)</p>
					<Button color="light">manage</Button>
				</div>
			</div>
			
		</div>

		<div class="bg-green-500"></div>
	</div>
</section>
