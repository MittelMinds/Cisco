<script>
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcomeFallback from '$lib/images/svelte-welcome.png';
	import {
		Navbar,
		NavBrand,
		NavLi,
		NavUl,
		NavHamburger,
		Textarea,
		Toolbar,
		ToolbarGroup,
		ToolbarButton,
		Button,
		Card,
		GradientButton
	} from 'flowbite-svelte';
	import Dashboard from '../lib/components/Dashboard.svelte';
	import {
		PaperClipOutline,
		MapPinAltSolid,
		ImageOutline,
		ArrowRightOutline,
		SearchOutline,
		FileLinesOutline
	} from 'flowbite-svelte-icons';
</script>

<svelte:head>
	<title>Dashbaord</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section class="">
	<!-- <div class="lg:h-24">
	</div> -->
	<h1 class="mb-4 text-5xl font-bold">Efficiency, supercharged.</h1>
	<h2 class="text-lg">We connect businesses that can profit from collaborating with each other.</h2>

	<div class="mt-6 flex flex-col space-y-4 lg:flex-row lg:space-x-4 lg:space-y-0">
		<div class="">
			<Card class="">
				<h2 class="mb-6 text-xl font-semibold text-black">What are you looking for?</h2>
				<form>
					<Textarea class="mb-4 lg:w-full" placeholder="You can type anything, it's like magic!">
						<div slot="footer" class="flex items-center justify-between">
							<Button href="chat" class="w-full" type="submit"><ArrowRightOutline /></Button>
						</div>
					</Textarea>
				</form>
				<p class="ms-auto text-xs text-gray-500 dark:text-gray-400">
					Our AI has been trained to help you find the best matches for your needs.
				</p>
			</Card>
		</div>

		<div class="flex w-1/3 flex-col space-y-2">
			<a href="offerEntryMethodSelection" class="h-1/2"
				><button
					type="button"
					class="mb-2 me-2 h-full w-full rounded-lg border border-gray-300 bg-white px-5 py-2.5 text-start text-sm font-medium text-gray-900 hover:bg-gray-100 focus:outline-none focus:ring-4 focus:ring-gray-100 dark:border-gray-600 dark:bg-gray-800 dark:text-white dark:hover:border-gray-600 dark:hover:bg-gray-700 dark:focus:ring-gray-700"
					>Use our Search Tool</button
				></a
			>

			<a href="offerEntryMethodSelection" class="h-1/2"
				><button
					type="button"
					class="mb-2 me-2 h-full w-full rounded-lg border border-gray-300 bg-white px-5 py-2.5 text-start text-sm font-medium text-gray-900 hover:bg-gray-100 focus:outline-none focus:ring-4 focus:ring-gray-100 dark:border-gray-600 dark:bg-gray-800 dark:text-white dark:hover:border-gray-600 dark:hover:bg-gray-700 dark:focus:ring-gray-700"
					>Offer a service</button
				></a
			>
		</div>

		<div class="outline outline-green-400 outline-1 rounded w-1/3 bg-grey-200 text-lg p-4">
			<p>Pool your resources, schedule costly training events together and bulk order supplies together with other businesses to save cost and valuable time. Our platform helps you identify and contact suitable partners.</p>
		</div>

		<!-- <div class="bg-amber-300 flex flex-col w-full">
			<div class="bg-red-200 h-1/2 flex items-center">
				<p class="ml-4">Search</p>
			</div>
			<div class="bg-red-200 h-1/2 flex items-center">
				<p class="ml-4">Offer a Service</p>
			</div>
		</div> -->
	</div>
	
</section>
