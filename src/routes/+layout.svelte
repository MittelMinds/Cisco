

<script>
	import Header from '../lib/components/Header.svelte';
	import '../app.css';
	import Sidebar from '$lib/components/Sidebar.svelte';
	

	let { children } = $props();
</script>

<div>
	<Header />

	<main id="background">
		{@render children()}
	</main>

	<!-- <footer>
		<p>
			Road to Start Hack, December 2024
		</p>
	</footer> -->
</div>

<style>

	#background{
		background-image: url("/src/lib/images/grainyGradient.jpg");
		background-attachment: fixed;
	}

	main {
		
		padding: 3rem;
		width: 100%;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
