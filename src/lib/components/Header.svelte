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
		DropdownDivider,
		Avatar,
		DropdownHeader
	} from 'flowbite-svelte';
	import { ChevronDownOutline } from 'flowbite-svelte-icons';
	import { SearchOutline, AtomOutline, BrainOutline } from 'flowbite-svelte-icons';
	$: activeUrl = $page.url.pathname;
</script>



<Navbar>
	<NavBrand href="/">
		<AtomOutline />
		<span class="ml-2 self-center whitespace-nowrap text-xl font-semibold dark:text-white"
			>SYNERGY</span
		>
	</NavBrand>

	<div class="flex items-center md:order-2">
		<Avatar id="avatar-menu" src="/src/lib/images/cat-avatar.png" />
		<NavHamburger class1="w-full md:flex md:w-auto md:order-1" />
	</div>

	<Dropdown class="w-fit" placement="bottom" triggeredBy="#avatar-menu">
		<DropdownHeader>
			<span class="block text-sm">John Smith</span>
		</DropdownHeader>
		<DropdownItem href="dashboard">My Dashboard</DropdownItem>
		<DropdownItem href="mybusiness">Settings</DropdownItem>
		<DropdownItem href="demo2">Demo 2</DropdownItem>
		<DropdownDivider />
		<DropdownItem>Sign out</DropdownItem>
	</Dropdown>
	<NavUl>
		
		<NavLi href="assistant" active={true}>AI Assistant</NavLi>
		<NavLi href="/" active={true}>Marketplace</NavLi>
		<NavLi href="dashboard" active={true}>Dashboard</NavLi>
		<NavLi href="/about">Our Mission</NavLi>
	</NavUl>
</Navbar>
