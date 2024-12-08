<script>
	import Dashboard from '/src/lib/components/Dashboard.svelte';

	import { page } from '$app/stores';
	import {
		Button,
		Sidebar,
		SidebarGroup,
		SidebarItem,
		SidebarWrapper,
		Badge,
		Indicator,
		Accordion,
		AccordionItem,
		MultiSelect
	} from 'flowbite-svelte';
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

	let types = [
		{ value: 'sup', name: 'Supply' },
		{ value: 'ser', name: 'Service' },
		{ value: 'oth', name: 'Other' }
	];

	let statuses = [
		{ value: 'ong', name: 'Ongoing', color: 'blue' },
		{ value: 'com', name: 'Completed', color: 'green' },
		{ value: 'ope', name: 'Open', color: 'dark' }
	];
</script>

<svelte:head>
	<title>Dashboard</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<div class="flex flex-row space-x-4">
		<div class="h-full w-fit">
			<Dashboard />
		</div>

		<div class="ml-4 w-2/3 rounded p-6 text-xl shadow-md outline outline-1 outline-gray-300">
			<Accordion flush multiple>
				<AccordionItem>
					<p slot="header" class="font-xl ml-2 text-black">AI Recommendations</p>
					<div
						class="h-fit w-fit rounded bg-gray-200 p-4 text-black outline outline-1 outline-gray-400"
					>
						<p class="text-md mb-2 flex flex-row">
							Epoxy Resin <ArrowRightOutline class="mx-2 mt-1" /> Adhesive Formulation
						</p>
						<p class="text-sm">Recommendation: Quality Control Innovation</p>
						<p class="mb-4 text-sm">Potential partners: 8</p>
						<div class="flex flex-row">
							<Button color="light">View Details</Button>
							<div class="grow"></div>
						</div>
					</div>
				</AccordionItem>
				<AccordionItem open>
					<p slot="header" class="font-xl ml-2 text-black">My Orders</p>
					<div class="mb-2 flex flex-row space-x-2 text-sm">
						<MultiSelect items={types} placeholder="Type" class="w-25 mb-2" />
						<MultiSelect items={statuses} placeholder="Status" class="mb-2" />
					</div>
					<div class="flex flex-row space-x-6 text-black">
						<div class="h-fit w-fit rounded bg-gray-200 p-4 outline outline-1 outline-gray-400">
							<p class="text-md mb-2">Cybersecurity Training</p>
							<p class="text-sm">Know - Die Fortbilder.</p>
							<Badge color="dark" rounded class="px-2.5 py-0.5">
								<Indicator color="dark" size="xs" class="me-1" />Service
							</Badge>
							<Badge color="blue" rounded class="mb-2 px-2.5 py-0.5">
								<Indicator color="blue" size="xs" class="me-1" />Ongoing
							</Badge>

							<Button color="light">View Details</Button>
						</div>
						<div class="h-fit w-fit rounded bg-gray-200 p-4 outline outline-1 outline-gray-400">
							<p class="text-md mb-2">Raw Material</p>
							<p class="text-sm">Roheisen Bayern AG</p>
							<Badge color="dark" rounded class="px-2.5 py-0.5">
								<Indicator color="dark" size="xs" class="me-1" />Supply
							</Badge>
							<Badge color="green" rounded class="mb-2 px-2.5 py-0.5">
								<Indicator color="green" size="xs" class="me-1" />Completed
							</Badge>
							<Button color="light">View Details</Button>
						</div>
					</div>
				</AccordionItem>
				<AccordionItem open>
					<p slot="header" class="font-xl ml-2 text-black">My Offers</p>
					<div class="flex flex-row space-x-6 text-black">
						<div class="h-fit w-fit rounded bg-gray-200 p-4 outline outline-1 outline-gray-400">
							<p class="text-md">Processed Metal</p>

							<Badge color="dark" rounded class="mb-2 px-2.5 py-0.5">
								<Indicator color="dark" size="xs" class="me-1" />Supply
							</Badge>
							<p class="mb-2 text-sm"><b>18</b> Clients</p>
							<Button color="light">View Orders</Button>
						</div>
						<div class="h-fit w-fit rounded bg-gray-200 p-4 outline outline-1 outline-gray-400">
							<p class="text-md">Machining</p>
							<Badge color="dark" rounded class="mb-2 px-2.5 py-0.5">
								<Indicator color="dark" size="xs" class="me-1" />Service
							</Badge>
							<p class="mb-2 text-sm"><b>7</b> Upcoming Appointments</p>
							<Button color="light">View Orders</Button>
						</div>
						<div class="h-fit w-fit rounded bg-gray-200 p-4 outline outline-1 outline-gray-400">
							<p class="text-md">Tool Sharpening</p>
							<Badge color="dark" rounded class="mb-2 px-2.5 py-0.5">
								<Indicator color="dark" size="xs" class="me-1" />Service
							</Badge>
							<p class="mb-2 text-sm"><b>2</b> Upcoming Appointments</p>
							<Button color="light">View Orders</Button>
						</div>
					</div>
				</AccordionItem>
				<AccordionItem open>
					<p slot="header" class="font-xl ml-2 text-black">Client Orders</p>
					<div class="mb-2 flex flex-row space-x-2 text-sm">
						<MultiSelect items={types} placeholder="Type" class="w-25 mb-2" />
						<MultiSelect items={statuses} placeholder="Status" class="mb-2" />
					</div>
					<div class="flex flex-row space-x-6 text-black">
						<div class="h-fit w-fit rounded bg-gray-200 p-4 outline outline-1 outline-gray-400">
							<p class="text-md">Gerhard Getriebe GmbH</p>

							<p class="text-sm">Processed Metal</p>
							<Badge color="dark" rounded class="mb-2 px-2.5 py-0.5">
								<Indicator color="dark" size="xs" class="me-1" />Supply
							</Badge>
							<Badge color="blue" rounded class="mb-2 px-2.5 py-0.5">
								<Indicator color="blue" size="xs" class="me-1" />Ongoing
							</Badge>
							<p class="mb-4 text-sm">Ordered on 07.12.2024</p>
							<Button color="light">View Details</Button>
						</div>
						<div class="h-fit w-fit rounded bg-gray-200 p-4 outline outline-1 outline-gray-400">
							<p class="text-md">Schmidt Manufaktur AG</p>

							<p class="text-sm">Tool Sharpening</p>
							<Badge color="dark" rounded class="mb-2 px-2.5 py-0.5">
								<Indicator color="dark" size="xs" class="me-1" />Service
							</Badge>
							<Badge color="green" rounded class="mb-2 px-2.5 py-0.5">
								<Indicator color="green" size="xs" class="me-1" />Completed
							</Badge>
							<p class="mb-4 text-sm">Completed on 08.12.2024</p>
							<Button color="light">View Details</Button>
						</div>
					</div>
				</AccordionItem>
			</Accordion>
		</div>
		<div class="bg-green-500"></div>
	</div>
</section>
