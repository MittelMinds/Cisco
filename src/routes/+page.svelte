<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcomeFallback from '$lib/images/svelte-welcome.png';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
</script>

<svelte:head>
	<title>Home home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<Navbar>
		<NavBrand href="/">
		  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTzJTZ4coqMYM5TqZceNVOu-M-issSAjZJ84Q&s" class="me-3 h-6 sm:h-9" alt="Flowbite Logo" />
		  <span class="self-center whitespace-nowrap text-black text-xl font-semibold dark:text-white">Flowbite</span>
		</NavBrand>
		<NavHamburger  />
		<NavUl >
		  <NavLi href="/">Home</NavLi>
		  <NavLi href="/about">About</NavLi>
		  <NavLi href="/docs/components/navbar">Navbar</NavLi>
		  <NavLi href="/pricing">Pricing</NavLi>
		  <NavLi href="/contact">Contact</NavLi>
		</NavUl>
	  </Navbar>
	<h1 class="text-3xl font-bold underline">
		hello there
	</h1>
	<h1>
		<span class="welcome">
			<picture>
				<source srcset={welcome} type="image/webp" />
				<img src={welcomeFallback} alt="Welcome" />
			</picture>
		</span>

		to your new<br />SvelteKit app
	</h1>

	<h2>
		try editing <strong>src/routes/+page.svelte</strong>
	</h2>

	<Counter />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
