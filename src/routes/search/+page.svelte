<script>
	import { Search, Button, Dropdown, DropdownItem } from 'flowbite-svelte';
	import { SearchOutline, ChevronDownOutline } from 'flowbite-svelte-icons';
    import ListingCard from '$lib/components/listingCard.svelte';

	const items = [
		{
			label: 'All categories'
		},
		{
			label: 'Mockups'
		},
		{
			label: 'Templates'
		},
		{
			label: 'Design'
		},
		{
			label: 'Logos'
		}
	];

	let selectCategory = 'All categories';
</script>

<form class="flex">
	<div class="relative">
		<Button class="whitespace-nowrap rounded-e-none border border-e-0 border-primary-700">
			{selectCategory}
			<ChevronDownOutline class="ms-2.5 h-2.5 w-2.5" />
		</Button>
		<Dropdown classContainer="w-40">
			{#each items as { label }}
				<DropdownItem
					on:click={() => {
						selectCategory = label;
					}}
					class={selectCategory === label ? 'underline' : ''}
				>
					{label}
				</DropdownItem>
			{/each}
		</Dropdown>
	</div>
	<Search
		size="md"
		class="rounded-none py-2.5"
		placeholder="Search for Suppliers, Services, Consultants..."
	/>
	<Button class="rounded-s-none !p-2.5">
		<SearchOutline class="h-6 w-6" />
	</Button>
</form>

<ListingCard title="Brass Milling" imgsrc="https://fraesteile-marktplatz.de/wp-content/uploads/2024/09/online-fertigung-messing-fraesen.webp" starcount=4 price="ab 25 EUR" prompt="jetzt anfragen"/>


