<script>
	import MyBusiness from "../MyBusinessTabs.svelte";
    import { Heading, P, A } from 'flowbite-svelte';
</script>
<svelte:head>
	<title>Home home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
    <Heading tag="h2" customSize="text-4xl font-extrabold ">MittelMinds GmbH</Heading>
    <MyBusiness/>
</section>