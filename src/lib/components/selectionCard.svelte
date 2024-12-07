<script>
	import { Card, Button } from 'flowbite-svelte';
	
    export let imgsrc;
    export let title;
    export let subtitle;
    export let buttonlabel;
</script>

<Card class="">
    <img class="h-28 w-28" src={imgsrc} alt="bot">
      <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">{title}</h5>
      <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">{subtitle}</p>
      <Button>
        {buttonlabel}
      </Button>
</Card>