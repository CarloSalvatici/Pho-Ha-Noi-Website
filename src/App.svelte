<script>
	export let name;
</script>

<main>
	<header class="bg-black py-5">
		<h1 class="text-white">Pho Ha Noi</h1>
	</header>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
		
	}

	header {
		background: black;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>