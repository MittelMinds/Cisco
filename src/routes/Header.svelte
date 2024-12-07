<script>
	import { page } from '$app/stores';
	import logo from '$lib/images/svelte-logo.svg';
	import github from '$lib/images/github.svg';

  	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, Button, Input } from 'flowbite-svelte';
	import { SearchOutline } from 'flowbite-svelte-icons';
  	$: activeUrl = $page.url.pathname;
</script>

<Navbar>
	<NavBrand href="/">
	  <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">Mittelstand Connect</span>
	</NavBrand>
	<div class="hidden relative md:block">
		<div class="flex absolute inset-y-0 start-0 items-center ps-3 pointer-events-none">
		  <SearchOutline class="w-4 h-4" />
		</div>
		<Input id="search-navbar" class="ps-10" placeholder="Search" />
	  </div>
	<div class="flex md:order-2">
	  <Button size="sm">Sign In</Button>
	  <NavHamburger />
	</div>
	<NavUl class="order-1">
	  <NavLi href="/" active={true}>Dashboard</NavLi>
	  <NavLi href="/about">Connect</NavLi>
	  <NavLi href="/docs/components/navbar">Business Relations</NavLi>
	  <NavLi href="/pricing">My Business</NavLi>
	</NavUl>
</Navbar>



