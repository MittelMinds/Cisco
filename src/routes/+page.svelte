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
	<h1
		class="animated-background mt-4 bg-gradient-to-r from-fuchsia-500 via-red-600 to-orange-400 bg-clip-text pb-4 text-5xl font-bold text-transparent"
	>
		Efficiency, supercharged.
	</h1>
	<h2 class="text-lg">We connect businesses that can profit from collaborating with each other.</h2>

	<div class="mt-8 flex flex-col space-y-4 lg:flex-row lg:space-x-4 lg:space-y-0">
		<div class="">
			<Card class="">
				<h2 class="mb-6 text-xl font-semibold text-black">What are you looking for?</h2>
				<form>
					<Textarea class="mb-4 lg:w-full" placeholder="You can type anything, it's like magic!">
						<div slot="footer" class="flex items-center justify-between">
							<Button color="dark" href="chat" class="w-full" type="submit"
								><ArrowRightOutline /></Button
							>
						</div>
					</Textarea>
				</form>
				<p class="ms-auto text-xs text-gray-500 dark:text-gray-400">
					Our AI has been trained to help you find the best matches for your needs.
				</p>
			</Card>
		</div>

		<div class="flex w-1/3 flex-col space-y-2">
			<a href="/" class="h-1/2"
				><button
					type="button"
					class="mb-2 me-2 h-full w-full rounded-lg border border-gray-300 bg-white px-5 py-2.5 text-start text-lg font-medium text-gray-900 hover:bg-gray-100 focus:outline-none focus:ring-4 focus:ring-gray-100 dark:border-gray-600 dark:bg-gray-800 dark:text-white dark:hover:border-gray-600 dark:hover:bg-gray-700 dark:focus:ring-gray-700"
					><p class="font-regular text-sm text-gray-500">Thinking about outsourcing?</p>
					Search our Marketplace</button
				></a
			>

			<a href="offerEntryMethodSelection" class="h-1/2"
				><button
					type="button"
					class="mb-2 me-2 h-full w-full rounded-lg border border-gray-300 bg-white px-5 py-2.5 text-start text-lg font-medium text-gray-900 hover:bg-gray-100 focus:outline-none focus:ring-4 focus:ring-gray-100 dark:border-gray-600 dark:bg-gray-800 dark:text-white dark:hover:border-gray-600 dark:hover:bg-gray-700 dark:focus:ring-gray-700"
					><p class="font-regular text-sm text-gray-500">Have something you'd like to offer?</p>
					Create a Listing</button
				></a
			>
		</div>

		<div class="bg-grey-200 w-1/3 rounded p-4 text-lg outline outline-1 outline-green-400">
			<p class="flex">
				<ArrowRightOutline class="mr-2 mt-1" />Pool your resources, schedule costly training events
				together and bulk order supplies with other businesses to save cost and valuable time. Our
				platform helps you identify and connect with suitable partners.
			</p>
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

	<!-- <div class="flex flex-row">
		<div
			class="mb-2 me-2 h-full w-full rounded-lg border border-gray-300 bg-white px-5 py-2.5 text-start text-lg font-medium text-gray-900 hover:bg-gray-100"
			><p class="font-regular text-sm text-gray-500">Thinking about outsourcing?</p>
			Search our Marketplace</div
		>

		<button
			type="button"
			class="mb-2 me-2 h-full w-full rounded-lg border border-gray-300 bg-white px-5 py-2.5 text-start text-lg font-medium text-gray-900 hover:bg-gray-100 focus:outline-none focus:ring-4 focus:ring-gray-100 dark:border-gray-600 dark:bg-gray-800 dark:text-white dark:hover:border-gray-600 dark:hover:bg-gray-700 dark:focus:ring-gray-700"
			><p class="font-regular text-sm text-gray-500">Thinking about outsourcing?</p>
			Search our Marketplace</button
		>
	</div> -->
</section>

<footer class="mt-96">
	<p>Road to Start Hack 2024</p>
</footer>
