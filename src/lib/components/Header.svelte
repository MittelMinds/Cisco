<script>
	import { page } from '$app/stores';
	import logo from '$lib/images/svelte-logo.svg';
	import github from '$lib/images/github.svg';

	import {
		Navbar,
		NavBrand,
		NavLi,
		NavUl,
		NavHamburger,
		Button,
		Input,
		Dropdown,
		DropdownItem,
		DropdownDivider
	} from 'flowbite-svelte';
	import { ChevronDownOutline } from 'flowbite-svelte-icons';
	import { SearchOutline, BrainOutline } from 'flowbite-svelte-icons';
	$: activeUrl = $page.url.pathname;
</script>

<Navbar>
	<NavBrand href="/">
		<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
			>Mittelstand Connect</span
		>
	</NavBrand>

	<div class="flex md:order-2">
		<Button size="sm"><BrainOutline class="mr-2 h-4 w-4" /> AI Assistant</Button>
		<NavHamburger />
	</div>
	<NavUl class="order-1">
		<NavLi href="/" active={true}>Dashboard</NavLi>

		<NavLi class="cursor-pointer">
			Connect
			<ChevronDownOutline class=" inline h-6 w-6 text-primary-800 dark:text-white" />
		</NavLi>
		<Dropdown class="z-20 w-44">
			<DropdownItem href="/">General Search</DropdownItem>
			<DropdownDivider />
			<DropdownItem href="/">Find Suppliers</DropdownItem>
			<DropdownItem href="/">Offer Supply</DropdownItem>
			<DropdownItem href="/">Find Service Provider</DropdownItem>
			<DropdownItem href="/">Find Other</DropdownItem>
		</Dropdown>

		<NavLi class="cursor-pointer">
			Business Relations
			<ChevronDownOutline class="inline h-6 w-6 text-primary-800 dark:text-white" />
		</NavLi>
		<Dropdown class="z-20 w-44">
			<DropdownItem href="/">All Business Relations</DropdownItem>
			<DropdownDivider />
			<DropdownItem href="/businessrelations">Current Suppliers</DropdownItem>
			<DropdownItem href="/businessrelations">Current Clients</DropdownItem>
			<DropdownItem href="/businessrelations">Current Service Provider</DropdownItem>
			<DropdownItem href="/businessrelations">Other Business Relations</DropdownItem>
		</Dropdown>

		<NavLi class="cursor-pointer">
			My Business
			<ChevronDownOutline class="inline h-6 w-6 text-primary-800 dark:text-white" />
		</NavLi>
		<Dropdown class="z-20 w-44">
			<DropdownItem href="/">My Business Profile</DropdownItem>
			<DropdownDivider />
			<DropdownItem href="/mybusiness">Settings</DropdownItem>
		</Dropdown>
	</NavUl>
</Navbar>
