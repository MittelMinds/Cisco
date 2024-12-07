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

		Card

	} from 'flowbite-svelte';
	import Dashboard from '../lib/components/Dashboard.svelte';
	import { PaperClipOutline, MapPinAltSolid, ImageOutline, ArrowRightOutline } from 'flowbite-svelte-icons';
</script>

<svelte:head>
	<title>Dashbaord</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section class="bg-amber-300">
	<!-- <div class="lg:h-24">
	</div> -->
	<h1 class="mb-4 text-5xl font-bold">Revolutionary efficiency for all.</h1>
	<h2 class="text-lg">Enterprise-level cost-savings for companies of all sizes.</h2>


<Card class="mt-6">
	<h2 class="text-xl text-black font-semibold mb-6">What are you looking for?</h2>
	<form>
		<Textarea class="mb-4 lg:w-full" placeholder="You can type anything, it's like magic!">
		  <div slot="footer" class="flex items-center justify-between">
			<Button type="submit"><ArrowRightOutline/></Button>
		  </div>
		</Textarea>
	  </form>
	  <p class="ms-auto text-xs text-gray-500 dark:text-gray-400">
		Our AI has been trained to help you find the best matches for your needs.
	  </p>

</Card>
	
</section>
