<script>
	import '../css/global.css';
	import Nav from '../components/Nav.svelte';
	import Footer from '../components/Footer.svelte';
</script>

<div class="app">
	<Nav />

	<div class="viewport">
		<main>
			<slot />
		</main>

		<Footer />
	</div>
</div>

<style>
	.app {
		display: flex;
		height: 100vh;
		width: 100vw;
	}

	.viewport {
		display: flex;
		flex-direction: column;
		flex: 1;
		height: inherit;
		background-color: #fbe1e1;
	}

	main {
		display: flex;
		flex: 1;
		width: 100%;
	}
</style>
