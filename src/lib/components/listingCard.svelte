<script>
	import { Card, Button, Rating, Badge } from 'flowbite-svelte';
    export let title;
    export let imgsrc;
    export var starcount;
    export let price;
    export let prompt;
</script>

<Card padding="lg">
	<a href="/">
		<img class="rounded-t-lg p-8 mb-8" src={imgsrc} alt="product 1" />
	</a>
	<div class="px-5 pb-5">
		<a href="/">
			<h5 class="text-xl font-semibold tracking-tight text-gray-900 dark:text-white">
				{title}
			</h5>
		</a>
		<Rating rating={starcount} size={24} class="mb-5 mt-2.5">
			<Badge slot="text" class="ms-3">{starcount}</Badge>
		</Rating>
		<div class="flex items-center justify-between">
			<span class="text-3xl font-bold text-gray-900 dark:text-white">{price}</span>
			<Button href="/">{prompt}</Button>
		</div>
	</div>
</Card>
