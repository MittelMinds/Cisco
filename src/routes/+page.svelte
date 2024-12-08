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
		SearchOutline
	} from 'flowbite-svelte-icons';
</script>

<svelte:head>
	<title>Dashbaord</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section class="">
	<!-- <div class="lg:h-24">
	</div> -->
	<h1 class="mb-4 text-5xl font-bold">Revolutionary efficiency for all.</h1>
	<h2 class="text-lg">Enterprise-level cost-savings for companies of all sizes.</h2>

	<div class="mt-6 flex flex-col lg:flex-row space-y-4 lg:space-y-0 lg:space-x-4">
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
		
		<div class="flex flex-col w-1/3 space-y-2">

			
				<button type="button" class="text-gray-900 bg-white border border-gray-300 focus:outline-none hover:bg-gray-100 focus:ring-4 focus:ring-gray-100 font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700 w-full h-1/2 text-start">Use our Search Tool</button>

				<button type="button" class="text-gray-900 bg-white border border-gray-300 focus:outline-none hover:bg-gray-100 focus:ring-4 focus:ring-gray-100 font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700 w-full h-1/2 text-start">Offer a service</button>
			

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
